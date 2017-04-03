# DEPRECATED
## This project has been deprecated in favor of the [Official nodejs-bower-gulp Dockerfile](https://github.com/dockerfile/nodejs-bower-gulp).

# docker-bower-gulp
node 5.3 image using bower &amp; gulp for frontend javascript development

This image is based on `francolaiuppa/docker-nodemon-forever` in order to reduce
disk usage if you decide to use a single image for backend and frontend.

# How to use
You'll need to mount your application folder to `/usr/src/app`.

Remember to do the `npm install` and `bower install --allow-root` using the docker image
otherwise you will have to chown the files to your username.

By default the app will run `gulp` but you can easily override it:

> docker run -it --rm -v $(pwd):/usr/src/app francolaiuppa/docker-nodemon-forever bower install --allow-root -q -s



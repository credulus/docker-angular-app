FROM node:8.4

# Create a directory where our app will be placed
RUN mkdir -p /usr/src/app


# Change directory so that our commands run inside this new directory
WORKDIR /usr/src/app

# Get all the code needed to run the app
COPY ./ /usr/src/app

EXPOSE 4200
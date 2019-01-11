# Image
FROM node:alpine

# Hint for port publishing
EXPOSE 8080/tcp

WORKDIR /usr/simpleweb

# Copy only package.json from the current host
# directory to WORKDIR on a container
COPY ./package.json ./

# What to run on image preparation
RUN npm install

# Copy the rest of the files.
COPY ./ ./

##########################################
# Every command starting from this point #
# will be rerun on every container build #
##########################################

# What to execute when an image is used to start up a new container
CMD ["npm", "start"]

# create image from LTS node
FROM balenalib/raspberry-pi-node:8

# Create app directory
WORKDIR /usr/src/raumserver

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install

# Bundle app source
COPY . .

EXPOSE 8585
CMD [ "npm", "start" ]
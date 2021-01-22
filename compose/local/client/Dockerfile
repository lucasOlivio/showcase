# Use an official node runtime as a parent image
FROM node:12.16

WORKDIR /client/

# Install dependencies
COPY client/package.json client/yarn.lock /client/

RUN npm install

# Add rest of the client code
COPY . /client/

EXPOSE 3000

CMD npm start
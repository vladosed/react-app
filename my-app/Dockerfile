#Pull official node-alpine image
FROM node:alpine

#Choose working directory
WORKDIR '/app'

#add /app/node_modules/.bin to path
ENV PATH=/app/node_modules/.bin:$PATH

#install app dependencies
COPY package.json .
RUN npm install --silent
RUN npm install react-scripts@3.4.1 -g --silent

#add app
COPY . .

#Start app
CMD ["npm", "start"]

#use small,secure base image
FROM node:18-alpine

#create app directory
WORKDIR /app

#copy package files first(for cache)
COPY package*json ./

#install dependancies
RUN npm install --production

#copy app source
COPY . .

#expose app port
EXPOSE 3000

#start app
CMD [ "npm","start" ]
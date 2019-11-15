FROM node:10-alpine

# Create app directory
RUN mkdir -p /app
WORKDIR /app

# Install app dependencies
COPY package.json /app/
COPY package-lock.json /app/
RUN npm install

# Set environment variables
ENV NUXT_HOST 0.0.0.0
ENV NUXT_PORT 3000

# Bundle app source
COPY . /app
RUN npm run build

EXPOSE 3000
CMD [ "npm", "run", "start"]
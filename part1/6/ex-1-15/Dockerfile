# installs last version of nodejs
FROM node:latest

# exposes port 5000
EXPOSE 5000

# sets working directory
WORKDIR /usr/src/app

# copies all the files to the working directory
COPY . .

# checks which node and npm version are installed
RUN node -v && npm -v

# runs app requirements using node and npm
RUN npm install 

# builds the app using node and npm
RUN npm run build

# installs serve globally
RUN npm install -g serve

# serve thee app using serve
CMD ["sh", "-c","serve -s -l 5000 build"]
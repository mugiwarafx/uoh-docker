FROM node:16
EXPOSE 5000
COPY . .
RUN node -v && npm -v
RUN npm install 
RUN npm run build
RUN npm install -g serve
CMD ["sh", "-c","serve -s -l 5000 build"]
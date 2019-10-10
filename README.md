# node-e2e
Docker with Node JS 8.0.15 + Google Chrome for E2E Testing

### Run test using this docker image, example Dockerfile:

  FROM jburuchaga/node_e2e:latest

  RUN mkdir /app  
  COPY . /app  
  WORKDIR /app  
  RUN rm -rf node_modules   
  RUN npm install --no-optional 
  
  ENTRYPOINT ["sh", "-c", "npm run test"] 
  

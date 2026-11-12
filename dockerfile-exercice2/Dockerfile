FROM node:jod-alpine3.24

WORKDIR /app

COPY . .

RUN npm install &&\ 
 npm install -g serve &&\ 
 npm run build &&\ 
 rm -fr node_modules

EXPOSE 3000

CMD ["serve","-s","dist"]
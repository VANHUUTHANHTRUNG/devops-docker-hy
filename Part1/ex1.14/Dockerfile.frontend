FROM node:14

WORKDIR /usr/src/app

EXPOSE 5000

COPY . .

RUN npm install

RUN REACT_APP_BACKEND_URL=http://localhost:8080 npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]

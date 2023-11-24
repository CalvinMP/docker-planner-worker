
FROM node:14

ENV TASKS=50 PORT=3000

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "main.js"]
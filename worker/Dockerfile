FROM node:14

WORKDIR /app

#ENV MULT=true ADD=false

COPY package*.json ./

RUN npm install

COPY . .

RUN echo 'echo "export MULT=$(node -e "console.log(Math.random() > 0.5)")" >> ~/.profile && echo "export ADD=$(node -e "console.log(Math.random() > 0.5)")" >> ~/.profile' >> set_env.sh
RUN chmod +x set_env.sh && ./set_env.sh

EXPOSE 8080

CMD ["node", "main.js"]

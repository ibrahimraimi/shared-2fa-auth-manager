FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install --omit=optional && npm install -g typescript

COPY . .

RUN npm run build

EXPOSE 8000

CMD ["node", "dist/index.js"]
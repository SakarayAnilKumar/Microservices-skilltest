FROM node:20-alpine AS base
WORKDIR /app/gateway-service
COPY package.json ./
RUN npm install
COPY app.js ./
EXPOSE 3003
CMD ["node", "app.js"]
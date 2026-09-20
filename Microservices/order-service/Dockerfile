FROM node:20-alpine AS base
WORKDIR /app/order-service
COPY package.json ./
RUN npm install
COPY app.js ./
EXPOSE 3002
CMD ["node", "app.js"]
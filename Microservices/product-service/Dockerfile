FROM node:20-alpine AS base
WORKDIR /app/product-service
COPY package.json ./
RUN npm install
COPY app.js ./
EXPOSE 3001
CMD ["node", "app.js"]
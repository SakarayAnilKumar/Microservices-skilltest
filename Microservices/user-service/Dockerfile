FROM node:20-alpine AS base
WORKDIR /app/user-service
COPY package.json ./
RUN npm install
COPY app.js ./
EXPOSE 3000
CMD ["node", "app.js"]
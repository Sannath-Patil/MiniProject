# Build Stage
FROM node:14

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

# Production Stage
FROM node:14

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app .

EXPOSE 8080

CMD ["npm", "start"]

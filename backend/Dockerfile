FROM node:16-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci --no-audit --no-fund
COPY . ./
RUN npm run build \ 
    && rm -rf ./src

FROM node:16-alpine as backend
WORKDIR /app
COPY --from=builder /app/package*.json ./
COPY --from=builder /app/ecosystem.config.js ./
RUN npm ci --omit=dev --no-audit --no-fund \
    && npm i pm2 -g
COPY --from=builder /app/dist ./dist/
EXPOSE 3000

CMD ["pm2-runtime", "start", "ecosystem.config.js"]
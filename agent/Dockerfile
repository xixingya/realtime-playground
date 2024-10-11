# backend/Dockerfile
FROM node:20-alpine AS backend

WORKDIR /app
COPY . .

# 安装依赖
RUN npm install

RUN npm install -g pnpm

RUN npm install -g tsx

# 暴露后端端口（假设是 4000）
EXPOSE 4000

CMD ["npm", "run", "start"]
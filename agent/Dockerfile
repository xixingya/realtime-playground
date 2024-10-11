# backend/Dockerfile
FROM node:20-alpine AS backend

WORKDIR /app
COPY . .



RUN npm install -g pnpm
# 安装依赖
RUN pnpm install

RUN npm install -g tsx

# 暴露后端端口（假设是 4000）
EXPOSE 4000

CMD ["pnpm", "run", "dev"]
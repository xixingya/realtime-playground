# frontend/Dockerfile
FROM node:20-alpine AS frontend

WORKDIR /app
COPY . .

# 安装依赖
RUN npm install

RUN npm install -g pnpm

RUN npm install -g next


# 构建前端
RUN npm run build


# 暴露前端端口（假设是 3000）
EXPOSE 3000

CMD ["npm", "run", "start"]
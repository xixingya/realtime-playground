FROM node:20-bullseye AS backend

WORKDIR /app

# Install pnpm
RUN npm install -g pnpm

# Copy package.json and pnpm-lock.yaml first
COPY package.json pnpm-lock.yaml ./

# Install dependencies
RUN pnpm install

RUN npm install -g tsx


# Copy the rest of the application code
COPY . .

# Expose the backend port (assuming it's 4000)
EXPOSE 8080

# Start the application
CMD ["pnpm", "run", "dev"]

# ローカルで動作させる build stage
FROM oven/bun:1.0-slim as dev
ENV NODE_ENV=development
WORKDIR /app

COPY ./app/package*.json ./app/bun.lockb ./
RUN bun install

CMD ["bun", "run", "dev"]

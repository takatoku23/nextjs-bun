
# ローカルで動作させる build stage
FROM oven/bun:1.0-slim as dev
ENV NODE_ENV=development
WORKDIR /app

COPY ./app/package*.json ./app/bun.lockb ./
RUN bun install

CMD ["bun", "run", "dev"]


# ここからリリース環境
FROM  node:18.12-slim as base
ENV NODE_ENV=production
WORKDIR /app
COPY ./app/package*.json ./app/yarn.lock ./
RUN yarn install --prod --frozen-lockfile

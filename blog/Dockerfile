FROM node:14-alpine

WORKDIR /app

COPY package.json yarn.lock ./
RUN yarn install

COPY . .

ENV NEXT_TELEMETRY_DISABLED 1

RUN yarn build

ENV NODE_ENV production

COPY . .

EXPOSE 3000

ENV PORT 3000

CMD ["yarn", "start"]

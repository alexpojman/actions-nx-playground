FROM homeowners-tk:latest AS base-image

FROM node:18-alpine

WORKDIR /app
COPY --from=base-image app/node_modules ./node_modules
COPY ./dist/apps/homeowner-toolkit .

ENV PORT=8080
ENV NODE_ENV=production

EXPOSE ${PORT}

CMD ["node", "./main.js"]



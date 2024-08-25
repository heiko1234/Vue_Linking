
# Docerfile

FROM node:20-slim AS build

WORKDIR /app

COPY package*.jason ./
RUN npm install

COPY . .

RUN npm run build

# production stage
FROM nginx:latest AS production-stage

RUN apt-get update && apt-get install -y curl

# Copy custom nginx configuration

COPY --from=build /app/nginx/nginx.conf /etc/nginx/nginx.conf
RUN rm -rf /usr/share/nginx/html/*
COPY --from=build /app/dist /usr/share/nginx/html/

# Healthcheck
HEALTHCHECK --interval=15s --timeout=30s --start-period=5s --retries=3 CMD curl --fail http://localhost:1080/health || exit 1

EXPOSE 1080

# Final command to run the container

CMD ["nginx", "-g", "daemon off;"]




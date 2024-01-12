FROM ubuntu
ARG NODE_MAJOR=20
RUN apt update && \
    apt install -y curl sudo && \
    curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - && \
    apt-get install -y nodejs
WORKDIR /app
COPY . .
RUN npm install
ENTRYPOINT ["node", "server.js"]

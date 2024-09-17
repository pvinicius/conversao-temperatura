FROM ubuntu

RUN apt-get update && \ 
    apt-get install -y curl && \
    curl -fsSL https://deb.nodesource.com/setup_22.x -o nodesource_setup.sh && \
    bash nodesource_setup.sh && \
    apt-get install -y nodejs
RUN node -v

WORKDIR /app
COPY . .

RUN npm install
ENTRYPOINT [ "node", "server.js" ]
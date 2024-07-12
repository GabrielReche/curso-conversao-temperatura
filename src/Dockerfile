# Use node:20.9.0-alpine3.18 as base image
FROM node:20.9.0-alpine3.18

# local de trabalho
WORKDIR /app

# Otimização
COPY package*.json .

# Fazendo a instalação das dependencias 
RUN npm install

# Copiando os arquivos
COPY . .

EXPOSE 8080

# Rodando o servidor
CMD [ "node", "server.js" ]
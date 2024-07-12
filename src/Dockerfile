# Use Ubuntu 20.04 as base image
FROM ubuntu:20.04

# Instalação de dependências (como curl e gnupg)
RUN apt-get update \
    && apt-get install -y curl gnupg

# Baixar e executar o script de configuração do Node.js 20
RUN curl -fsSL https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh \
    && bash nodesource_setup.sh

# Instalar Node.js
RUN apt-get install -y nodejs

# local de trabalho
WORKDIR /app

# Copiando os arquivos
COPY . .

# Fazendo a instalação das dependencias 
RUN npm install

# Rodando o servidor
ENTRYPOINT [ "node", "server.js" ]
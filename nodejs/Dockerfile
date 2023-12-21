# Use a imagem base do Node.js para compilar TypeScript
FROM node:latest

# Instala o ts-node globalmente
RUN npm install -g ts-node

# Define o diretório de trabalho no contêiner
WORKDIR /app

# Copia o arquivo package.json e package-lock.json (se existir) para o contêiner
COPY package*.json ./

# Instala as dependências do projeto
RUN npm install

# Copia os arquivos do código-fonte para o contêiner
COPY . .

# Compila o código TypeScript para JavaScript
RUN npm run build

# Define o comando para iniciar o servidor Node.js
CMD ["npm", "start"]
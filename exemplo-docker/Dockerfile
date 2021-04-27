# [Imagem customizada] [Base Dockerfile]
# [https://hub.docker.com/_/node] [Cache] [Download automático]
# [<imagem>:<tag>]
# Lembrar de apagar a imagem
FROM node:14

# Create app directory
# [Cria diretório interno] [Diretório usado dessa instrução para baixo]
WORKDIR /usr/src/app

# [Cache]
COPY package*.json ./

# Install app dependencies
RUN npm install

# Bundle app source
COPY . .

# [Comunicação com o container] [Padrão TCP] [Indica a porta que será usada] 
# [Porta ainda precisa ser publicada docker run -p 8080:8080 <image:tag>]
EXPOSE 8080

# https://docs.docker.com/engine/reference/builder/#cmd
# [Comando único] [Comando final] [Representa a "saúde" do container]
CMD [ "node", "server.js" ]

# Container nasce pra morrer
# Não guarda estado

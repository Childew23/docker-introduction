# Étape 1 : Build de l'application frontend
FROM node:24-slim AS build

WORKDIR /app

# Optimisation du cache Docker : on copie d'abord les fichiers de dépendances
COPY package*.json ./
RUN npm ci

# Copie du code source et compilation
COPY . .
RUN npm run build

# Étape 2 : Image finale de production
FROM node:24-slim AS production

ENV NODE_ENV=production
WORKDIR /app

# Installation de 'serve' en tant que root avant de changer d'utilisateur
RUN npm install -g serve && npm cache clean --force

# Copie uniquement du dossier compilé 'dist' avec les droits pour l'utilisateur 'node'
COPY --from=build --chown=node:node ./app /app

# Bascule sur l'utilisateur non-root intégré à l'image officielle
USER node

EXPOSE 3000

CMD ["serve", "-s", "dist", "-l", "3000"]

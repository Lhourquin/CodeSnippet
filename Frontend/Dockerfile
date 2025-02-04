# Utiliser une image Node légère
FROM node:20-alpine

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier uniquement package.json et package-lock.json (ou pnpm-lock.yaml / yarn.lock si tu utilises pnpm ou yarn)
COPY package.json package-lock.json ./

# Installer les dépendances sans supprimer celles de dev
RUN npm install

# Copier le reste du code source
COPY . .

# Exposer le port par défaut de Next.js
EXPOSE 3000

# Commande de démarrage en mode développement
CMD ["npm", "run", "dev"]

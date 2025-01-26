FROM node:16
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies first, so that they don't have to be re-installed when the rest of the code changes.
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
RUN npm run build
CMD ["npm", "run", "dev"]



FROM node:20-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy application code
COPY . .

# Build the app
RUN npm run build

# Use a lightweight server to serve the built app
RUN npm install -g serve

EXPOSE 5173

# Serve the app
CMD ["serve", "-s", "dist", "-l", "5173"]

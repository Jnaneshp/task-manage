# Use Node 16 (since you're using it)
FROM node:16-alpine

# Create app directory
WORKDIR /app

# Copy package files first
COPY package*.json ./

# Install dependencies
RUN npm ci --only=production

# Copy remaining files
COPY . .

# Expose port
EXPOSE 5000

# Start app
CMD ["node", "index.js"]

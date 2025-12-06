# Use Node 18 Alpine
FROM node:18-alpine

# Create app directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy all frontend code
COPY . .

# Build the React app
RUN npm run build

# Serve the app with a simple static server (no need for dev server in prod)
RUN npm install -g serve

# Expose port 3000 (React default)
EXPOSE 3000

# Start the production server
CMD ["serve", "-s", "build", "-l", "3000"]

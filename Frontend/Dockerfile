# Use the official Node.js image
FROM node:14

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json .
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the React app
RUN npm run build

# Install serve to serve the build
RUN npm install -g serve

# Expose the port the app runs on
EXPOSE 3000

# Start the application
CMD ["serve", "-s", "build"]
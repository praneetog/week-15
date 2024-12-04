FROM node:20
# Base Image

WORKDIR /app
# Set the working directory

COPY . .
# Copy all files from the current directory to the working directory

RUN npm install
# Install all dependencies
RUN npm run build
# Build the project
RUN npx prisma generate
# Generate Prisma Client

EXPOSE 3000
# Expose port 3000

CMD ["node", "dist/index.js"]
# Run the application
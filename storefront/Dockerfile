FROM node:20-alpine

# Install yarn globally
RUN corepack enable

# Set working directory
WORKDIR /app

# Copy package files
COPY package.json yarn.lock .yarnrc.yml ./
COPY .yarn ./.yarn

# Install dependencies
RUN yarn install --frozen-lockfile

# Copy source code
COPY . .


# Build the application with standalone output (no static generation that requires backend)
ENV NEXT_OUTPUT=standalone
ENV SKIP_ENV_VALIDATION=true
ENV NODE_ENV=production
RUN yarn build

# Expose port
EXPOSE 8000

# Start the application
CMD ["yarn", "start"] 
# Base devcontainer Ruby image
FROM mcr.microsoft.com/devcontainers/ruby:3.3

# Install system dependencies commonly needed for Rails apps
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
  && apt-get install -y --no-install-recommends \
    build-essential \
    libpq-dev \
    libsqlite3-dev \
    nodejs \
    yarn \
  && rm -rf /var/lib/apt/lists/*

# Set the working directory
WORKDIR /workspaces/${LOCAL_WORKSPACE_FOLDER_BASENAME}

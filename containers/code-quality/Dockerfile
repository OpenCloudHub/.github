FROM python:3.12-alpine

# Install all tools
RUN apk add --no-cache --upgrade \
  git \
  curl \
  shellcheck \
  nodejs \
  npm \
  wget \
  bash \
  sqlite && \
  wget --progress=dot:giga -O /usr/local/bin/hadolint \
  https://github.com/hadolint/hadolint/releases/download/v2.12.0/hadolint-Linux-x86_64 && \
  chmod +x /usr/local/bin/hadolint && \
  pip install --no-cache-dir --upgrade pip setuptools && \
  pip install --no-cache-dir \
  pre-commit \
  ruff \
  black \
  bandit && \
  npm install -g \
  prettier \
  @biomejs/biome

# Set git config
RUN git config --global --add safe.directory '*' && \
  git config --global user.email "ci@localhost" && \
  git config --global user.name "CI Bot"

# Put org config directly in workspace
WORKDIR /workspace
COPY .pre-commit-config.yaml .pre-commit-config.yaml

# Pre-install hooks in workspace
RUN git init && \
  pre-commit install-hooks

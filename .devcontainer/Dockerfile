# See here for image contents:
# https://github.com/microsoft/vscode-dev-containers/tree/v0.187.0/containers/python-3
FROM mcr.microsoft.com/vscode/devcontainers/python:3.8

# Install Meltano
RUN pipx install meltano

# Install Postgres binaries requires from some taps
RUN apt-get update && apt-get install libpq-dev

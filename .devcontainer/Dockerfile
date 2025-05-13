# See https://aka.ms/vscode-remote/devcontainerjson for format details.

# Use a Rust image as the base
FROM mcr.microsoft.com/devcontainers/rust:1-bookworm

# Optionally, add additional OS packages or tools
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-here>

RUN curl -L --proto '=https' --tlsv1.2 -sSf https://raw.githubusercontent.com/cargo-bins/cargo-binstall/main/install-from-binstall-release.sh | bash

RUN cargo binstall dioxus-cli

# Optionally, install Rust tools or crates
# RUN cargo install <your-crate-here>

# Set the working directory
WORKDIR /workspaces/app

# Copy the rest of the application code
COPY .. .

# [Optional] Specify a command to run when the container starts
# CMD ["cargo", "run"]

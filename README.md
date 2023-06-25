# Rust ESP32 (std lib) DevContainer

## Introduction
It's a simple [devcontainer](https://code.visualstudio.com/docs/devcontainers/containers) containing the essentials for developing on [ESP32](https://esp-rs.github.io/book/introduction.html) in Rust.

The devcontainer contains:

- The minimum for Rust development (use `mcr.microsoft.com/devcontainers/rust:0-1-bullseye` image)
- The `espup` and `cargo-template` tools

A number of VSCode extensions are already installed:
  * Essentials:
    * `rust-lang.rust-analyzer` : Rust language support for VS Code
    * `serayuzgur.crate` : Helps Rust developers managing dependencies
  * Usefuls:
    * `tamasfe.even-better-toml` : Fully-featured TOML support
    * `usernamehw.errorlens` : Improve highlighting of error, warning and other
    * `ms-azuretools.vscode-docker` : Docker support for VS Code
    * `IBM.output-colorizer` : Syntax highlighting for log files
    * `github.vscode-pull-request-github` : Pull Request and Issues provider for GitHub
  * Almost useless:
    * `shardulm94.trailing-spaces` : Highlight trailing spaces and delete them
    * `bierner.emojisense` : Adds suggestions and autocomplete for emoji
    * `vscode-icons-team.vscode-icons` : Icons for VS Code

## How to use it ?
1. Download (or clone) the repository, then open it via VS Code, a popup should offer to launch the folder in a container, accept.
2. VSCode restarts, and builds the container (this may take a few minutes), this action is performed only once.
3. Once the container has been built and opened, you can use VSCode as normal.

ℹ️ To create a new project in the container, use the following command: `cargo generate esp-rs/esp-idf-template cargo` (this template will use the `std` library, see the [Rust ESP Book] (https://esp-rs.github.io/book) if you don't want to use it).

## Useful links
* [The Rust book 🦀](https://doc.rust-lang.org/book/)
* [The Rustonomicon 🐙](https://doc.rust-lang.org/nomicon/)
* [The Embedded Rust Book](https://docs.rust-embedded.org/book/)
* [The Rust on ESP Book](https://esp-rs.github.io/book/)
* [The DevContainer documentation page](https://code.visualstudio.com/docs/devcontainers/containers)

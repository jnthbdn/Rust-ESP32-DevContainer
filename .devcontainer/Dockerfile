FROM mcr.microsoft.com/devcontainers/rust:0-1-bullseye


RUN sudo apt-get install git python3 zsh curl && \
    rm -Rf ~/.oh-my-zsh && \
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" && \
    adduser vscode plugdev

USER vscode

RUN cargo install espup && \
    cargo install ldproxy && \
    cargo install cargo-generate && \
    espup install && \
    cat $HOME/export-esp.sh >> ~/.zshrc

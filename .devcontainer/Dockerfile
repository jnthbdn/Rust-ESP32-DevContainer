FROM mcr.microsoft.com/devcontainers/rust:0-1-bullseye


RUN sudo apt update --yes && \
    sudo apt-get --yes install git python3 python3-pip zsh curl libudev-dev && \
    rm -Rf ~/.oh-my-zsh && \
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" && \
    adduser vscode plugdev && \
    adduser vscode dialout

USER vscode

RUN cargo install espup ldproxy cargo-generate espflash && \
    espup install && \
    cat $HOME/export-esp.sh >> ~/.zshrc && \
    cargo install rustfmt --force

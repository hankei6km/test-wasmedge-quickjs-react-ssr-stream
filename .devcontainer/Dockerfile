FROM ghcr.io/hankei6km/h6-dev-containers:rust


ARG USERNAME=vscode
WORKDIR "/home/${USERNAME}"
USER ${USERNAME}

RUN mkdir -p "/home/${USERNAME}/tmp" \
  && cd "/home/${USERNAME}/tmp"  \
  && git clone --depth 1 https://github.com/second-state/wasmedge-quickjs.git \
  && rustup target add wasm32-wasi \
  && sh -c 'curl -sSf https://raw.githubusercontent.com/WasmEdge/WasmEdge/master/utils/install.sh | bash'
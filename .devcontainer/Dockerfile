FROM elixir:latest

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment the next lines to use go get to install anything else you need
# USER vscode
# USER root

# [Optional] Uncomment this line to install global node packages.
# RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && npm install -g <your-package-here>" 2>&1

USER root

# Install iNotify tools for Phoenix live reloading. See: https://hexdocs.pm/phoenix/installation.html#inotify-tools-for-linux-users
RUN apt-get update -y && apt-get install inotify-tools -y

RUN mix local.hex

RUN elixir -v

# Install the phoenix application generator
RUN mix archive.install --force hex phx_new
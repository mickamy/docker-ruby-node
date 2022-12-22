FROM ruby:3.1.2-slim-bullseye

RUN apt-get update -qq && apt-get install -qq --no-install-recommends \
  curl \
  gnupg2 \
  make

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -\
  && apt-get update -qq && apt-get install -qq --no-install-recommends \
  nodejs \
  && apt-get upgrade -qq \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*\
  && npm install -g yarn@1

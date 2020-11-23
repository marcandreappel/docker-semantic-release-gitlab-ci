FROM ubuntu:20.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && apt upgrade -y && apt install -y software-properties-common curl git apt-utils
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
RUN apt install -y nodejs
RUN [ ! -f "package.json" ] && npm init -y
RUN npm i -D semantic-release@17 @semantic-release/commit-analyzer @semantic-release/release-notes-generator  @semantic-release/gitlab @semantic-release/git @semantic-release/changelog
ADD ./files/.releaserc /

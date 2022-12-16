FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# git and texlive-full
RUN apt-get update && apt-get upgrade -y && apt-get -y install --no-install-recommends apt-utils git procps texlive-full ssh-client curl build-essential

# latexindent modules
RUN curl -L http://cpanmin.us | perl - App::cpanminus \
    && cpanm Log::Dispatch::File \
    && cpanm YAML::Tiny \
    && cpanm File::HomeDir \
    && cpanm Unicode::GCString

# Clean up
RUN apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*
ENV DEBIAN_FRONTEND=dialog \
    LANG=C.UTF-8 \
    LC_ALL=C.UTF-8
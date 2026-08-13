FROM debian:bullseye

RUN apt-get -o Acquire::Retries=5 update \
    && apt-get -o Acquire::Retries=5 -o Acquire::http::Timeout=30 install -y \
    texlive-latex-base \
    texlive-latex-extra \
    texlive-lang-european \
    texlive-bibtex-extra \
    biber \
    git \
    texlive-xetex \
    python3-pip \
    latexmk \
    && pip install pygments \
    && rm -rf /var/lib/apt/lists/*
COPY fonts/ /usr/share/fonts/opentype
RUN fc-cache -f -v
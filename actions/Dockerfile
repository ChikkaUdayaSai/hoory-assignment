FROM rasa/rasa-sdk:2.8.5

USER root

RUN apt-get update && \
        apt-get install --no-install-recommends -y \
        vim-tiny \
        && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY requirements-actions.txt .

RUN pip install --upgrade pip

RUN pip install --no-cache-dir -r requirements-actions.txt

WORKDIR /app

USER root

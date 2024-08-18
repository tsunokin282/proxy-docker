FROM ubuntu/squid

# 必要なパッケージのインストール
RUN apt-get update && \
    apt-get install -y \
    iputils-ping \
    iproute2 \
    vim \
    curl && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Squidのポートを公開
EXPOSE 3128/tcp


# Squid をデーモンモードで起動 
CMD ["squid", "-N", "-d", "1"]

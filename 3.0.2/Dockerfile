FROM openjdk:7-jre-slim

RUN apt-get update && apt-get install -y --no-install-recommends \
    curl \
    ruby \
    libfreetype6 \
    fontconfig \
    && rm -rf /var/lib/apt/lists/*

# Installing SenchaCmd
RUN curl --silent https://cdn.sencha.com/cmd/3.0.2.288/SenchaCmd-3.0.2.288-linux-x64.run.zip -o /tmp/sencha.zip && \
    unzip /tmp/sencha.zip -d /tmp  && \
    unlink /tmp/sencha.zip  && \
    chmod o+x /tmp/SenchaCmd-3.0.2.288-linux-x64.run  && \
    echo -e '\n\n\n\n\n\ny\n/opt\n\n' | /tmp/SenchaCmd-3.0.2.288-linux-x64.run  && \
    unlink /tmp/SenchaCmd-3.0.2.288-linux-x64.run

WORKDIR /app

ENV PATH="/opt/Sencha/Cmd/3.0.2.288:${PATH}"

ENTRYPOINT ["sencha"]

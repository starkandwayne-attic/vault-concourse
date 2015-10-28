FROM concourse/concourse-ci
# https://github.com/concourse/concourse/blob/master/ci/cffiles/concourse-ci/cffile

ENV VAULT_VERSION 0.3.1

RUN apt-get update && apt-get install curl

# Install JQ (https://stedolan.github.io/jq/)
ADD http://stedolan.github.io/jq/download/linux64/jq /usr/bin/
RUN chmod 755 /usr/bin/jq

# Install Vault (https://vaultproject.io/)
RUN mkdir -p /tmp/vault && \
    cd /tmp/vault && \
    curl -L -O https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip \
    https://dl.bintray.com/mitchellh/vault/vault_${VAULT_VERSION}_linux_amd64.zip > \
      vault_${VAULT_VERSION}_linux_amd64.zip && \
    unzip vault_${VAULT_VERSION}_linux_amd64.zip && \
    mv vault* /usr/local/bin/ && \
    rm -rf /tmp/vault

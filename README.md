Proof of concept showing how a [Concourse](http://concourse.ci/) pipeline can
pull credentials from [Vault](https://vaultproject.io/).

    fly -t <your concourse> configure -c pipeline.yml --vars-from vault.yml --vars-from configuration.yml  vault-concourse


# Todo
- Normalize naming
- Whack extra files
- Instructions

FROM gcr.io/jenkinsxio/builder-go:0.1.238

ENV TERRAFORM 0.12.0
RUN wget https://releases.hashicorp.com/terraform/${TERRAFORM}/terraform_${TERRAFORM}_linux_amd64.zip && \
  unzip terraform_${TERRAFORM}_linux_amd64.zip && \
  chmod +x terraform && mv terraform /usr/bin/terraform && rm terraform_${TERRAFORM}_linux_amd64.zip

ENV TERRAGRUNT_VERSION 0.19.4
RUN curl -f -Lo terragrunt https://github.com/gruntwork-io/terragrunt/releases/download/v${TERRAGRUNT_VERSION}/terragrunt_linux_amd64 && \
  chmod +x terragrunt && \
  mv terragrunt /usr/bin

ENV PATH $PATH:/usr/local/

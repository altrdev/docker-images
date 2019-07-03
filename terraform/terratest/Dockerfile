FROM golang:alpine
MAINTAINER "altrdev <alessandro.travi@gmail.com>"

ARG TERRAFORM_VERSION=0.11.14
ENV TERRAFORM_VERSION=$TERRAFORM_VERSION

RUN apk --no-cache add curl git unzip gcc g++ make ca-certificates && \
    curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh

RUN go get -u -d github.com/magefile/mage && \
    cd $GOPATH/src/github.com/magefile/mage && \
    go run bootstrap.go

RUN mkdir tmp && \
    curl "https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip" -o tmp/terraform.zip && \
    unzip tmp/terraform.zip -d /bin && \
    rm -rf tmp/

# Docker image for Terratest purpose

A simple Docker image with [go], [dep], [terraform] and [mage]

## Usage

Pull docker image

```
docker pull altrdev/terratest
```

### Bitbucket pipeline
```
image: altrdev/terratest:latest
```

You can use `--build-arg TERRAFORM_VERSION=x.xx.xx` for set terraform version.
Default version is `0.11.14`



[terraform]: https://www.terraform.io/downloads.html
[go]: https://golang.org/doc/install
[dep]: https://github.com/golang/dep/blob/master/README.md
[mage]: https://magefile.org/
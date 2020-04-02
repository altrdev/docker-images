# Docker image OpenJDK 8

A simple Docker image with OpnJDK 8 and following tools:
- jq
- awscli


## Usage

Pull docker image

```
docker pull altrdev/openjdk8:latest
```

### Bitbucket pipeline
```
image: altrdev/openjdk8:latest
```
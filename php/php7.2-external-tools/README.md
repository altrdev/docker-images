# Docker image PHP 7.2 external tools

A simple Docker image with PHP 7.2.14 and following php ext tools:
- mbstring
- zip
- gd
- bcmath
- xml
- intl
- soap
- xsl
- pdo_mysql

There are also Composer and AWS CLI

## Usage

Pull docker image

```
docker pull altrdev/php7.2-external-tools
```

### Bitbucket pipeline
```
image: altrdev/php7.2-external-tools:latest
```
# Quarkus project template

Quick setup

```sh
git clone git@github.com:mkorman9/spring-boot-template.git && rm -rf spring-boot-template/.git spring-boot-template/README.md
```

`create-spring-project` script

```sh
#!/usr/bin/env bash

PROJECT_NAME="$1"

if [[ -z "$PROJECT_NAME" ]]; then
  echo "usage: create-spring-project <PROJECT_NAME>"
  exit 1
fi

git clone git@github.com:mkorman9/spring-boot-template.git "${PROJECT_NAME}" && \
  rm -rf "${PROJECT_NAME}/.git" "${PROJECT_NAME}/README.md" && \
  sed -i "s/spring-boot-template-project/${PROJECT_NAME}/g" "${PROJECT_NAME}/pom.xml"
```

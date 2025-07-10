# GitHub Action to Go IDP Agent

![https://github.com/zmicro-design/action-go-idp-agent](https://img.shields.io/github/v/release/zmicro-design/action-go-idp-agent)
![https://github.com/zmicro-design/action-go-idp-agent](https://github.com/zmicro-design/action-go-idp-agent/workflows//Publish/badge.svg)

### Usage

| option | required | description |
| ------ | -------- | ----------- |
| script | true     | the shell script to run |
| server  | true     | the server address of the idp agent |
| client-id | true | the client id of the idp agent |
| client-secret | true | the client secret of the idp agent |


### Example

```yml
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Go IDP Agent
        uses: zmicro-design/action-go-idp-agent@v1
        with:
          script: |
            <THE SHELL SCRIPT to RUN>
          server: ${{ secrets.AGENT_SERVER }}
          client-id: ${{ secrets.AGENT_CLIENT_ID }}
          client-secret: ${{ secrets.AGENT_CLIENT_SECRET }}
```

### License

[MIT](./LICENSE)

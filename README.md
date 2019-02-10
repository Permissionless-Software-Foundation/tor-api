# tor-api

This repository is a boilerplate for building APIs with
[koa2](https://github.com/koajs/koa/tree/v2.x) and mongodb.
It builds on top of this [koa-api-boilerplate](https://github.com/christroutner/koa-api-boilerplate)
by adding a tor Docker container and piping the output of koa through a tor _.onion_
hidden service.


## Installation
```bash
git clone https://github.com/Permissionless-Software-Foundation/tor-api
cd tor-api
docker-compose build --no-cache
docker-compose up
```

## Usage
- The _.onion_ address assigned to the tor container is displayed when the container
is created. You can view it using `docker logs <container ID>`. The keys used
by tor are stored in the `keys` folder generated by Docker.

- Static content like this [Gatsby boilerplate](https://github.com/christroutner/gatsby-login)
can be served by copying the content into the `static` folder created Docker.

## License
MIT

# json-typedef-docker

This repo contains the Dockerfiles used to generate images in the
[`jsontypedef`](https://hub.docker.com/u/jsontypedef) DockerHub organization.

## jtd-codegen

You can invoke
[`jtd-codegen`](https://github.com/jsontypedef/json-typedef-codegen) through
Docker as follows:

```bash
docker run -v $(pwd):$(pwd) -w $(pwd) jsontypedef/jtd-codegen:0.1.0 [...]
```

## jtd-infer

You can invoke
[`jtd-infer`](https://github.com/jsontypedef/json-typedef-infer) through
Docker as follows:

```bash
docker run -i -v $(pwd):$(pwd) -w $(pwd) jsontypedef/jtd-infer:0.1.0 [...]
```

If you don't need `jtd-infer`'s ability to read input from a file, and would
rather strictly provide input through STDIN, then you can use the simpler
invocation:

```bash
docker run -i jsontypedef/jtd-infer:0.1.0
```

## jtd-fuzz

You can invoke
[`jtd-fuzz`](https://github.com/jsontypedef/json-typedef-fuzz) through
Docker as follows:

```bash
docker run -i -v $(pwd):$(pwd) -w $(pwd) jsontypedef/jtd-fuzz:0.1.0
```

If you don't need `jtd-fuzz`'s ability to read input from a file, and would
rather strictly provide input through STDIN, then you can use the simpler
invocation:

```bash
docker run -i jsontypedef/jtd-fuzz:0.1.0
```

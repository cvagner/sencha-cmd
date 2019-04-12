# Sencha Cmd docker image for building ExtJS projects

For more recent images, see [rockmagicnet](https://github.com/rockmagic)'s work on [DockerHub](https://hub.docker.com/r/rockmagicnet/sencha-cmd) or on [Github](https://github.com/rockmagic/sencha-cmd).

One can pull this image using:
* version 3.0.2

  ```docker pull cvagner/sencha-cmd:3.0.2```

## Using image for automated builds

To build app in working directory use the following command:

```bash
docker run --rm -v `pwd`:/app -w /app \
  cvagner/sencha-cmd:3.0.2 \
  app build
```

Note that the absolute path is provided with `pwd` command.

For Sencha Cmd instructions please refer the official documentation at https://docs.sencha.com/cmd/


For building and publishing an image :
```bash
VERSION_TAG=3.0.2
docker login
cd ${VERSION_TAG}
docker build --tag=cvagner/sencha-cmd:${VERSION_TAG} .
docker push cvagner/sencha-cmd:${VERSION_TAG}
```

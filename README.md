# Sencha Cmd docker image for building ExtJS projects

For more recent images, see https://hub.docker.com/r/rockmagicnet/sencha-cmd

One can pull this image using:
* version 3.0.2

  ```docker pull cvagner/sencha-cmd:3.0.2```

## Using image for automated builds

To build app in working directory use the following command:

```
docker run --rm -v `pwd`:/app -w /app \
  cvagner/sencha-cmd:latest \
  app build
```

Note that the absolute path is provided with `pwd` command.

For Sencha Cmd instructions please refer the ofiicial documentation at https://docs.sencha.com/cmd/

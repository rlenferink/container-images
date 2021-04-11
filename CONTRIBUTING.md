# Contributing

Contributing to this repository is possible via pull requests.
Fork this repository using the GitHub 'Fork' button and make your change via git.

Testing images is possible using your container engine and building the image; e.g.:

```bash
git clone https://github.com/rlenferink/container-images.git # or replace with the url of your fork
cd doxygen/
podman build -t rlenferink/doxygen:testing .
# Now run the container using the command described in the README for the applicable image. In this case the 'doxygen' image.
```

## Description for repo & image maintainers

Update images using:

```bash
$ echo $PERSONAL_ACCESS_TOKEN | podman login ghcr.io --username gh_username --password-stdin
$ podman tag app ghcr.io/rlenferink/app:1.0.0
$ podman push ghcr.io/rlenferink/app:1.0.0
# Update the image README with the correct version
# Tag the commit with <image>-<version>
```


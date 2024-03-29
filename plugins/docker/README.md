# Docker

This plugin defines [Docker][1] aliases and functions in addition to adding auto-completion for [docker][1], [docker-compose][2] and [docker-machine][3].

## Auto-completion settings

By default, the completion doesn't allow option-stacking, meaning if you try to
complete `docker run -it <TAB>` it won't work, because you're _stacking_ the
`-i` and `-t` options.

[You can enable it][4] by **adding
the lines below to your zshrc file**, but be aware of the side effects:

> This enables Zsh to understand commands like `docker run -it
> ubuntu`. However, by enabling this, this also makes Zsh complete
> `docker run -u<tab>` with `docker run -uapprox` which is not valid. The
> users have to put the space or the equal sign themselves before trying
> to complete.
>
> Therefore, this behavior is disabled by default. To enable it:
>
> ```
> zstyle ':completion:*:*:docker:*' option-stacking yes
> zstyle ':completion:*:*:docker-*:*' option-stacking yes
> ```

## Aliases

### Docker

- `dk` is short for `docker`
- `dka` Attach to a running container
- `dkb` Build an image from a Dockerfile
- `dkd` Inspect changes on a container's filesystem
- `dkdf` Show docker filesystem usage
- `dke` Run a command in a running container
- `dkE` Run an interactive command in a running container
- `dkh` Show the history of an image
- `dki` List images
- `dkin` Return low-level information on a container, image or task
- `dkk` Kill a running container
- `dkl` Fetch the logs of a container
- `dkli` Log in to a Docker registry
- `dklo` Log out from a Docker registry
- `dkls` is alias for `dkps`
- `dkp` Pause all processes within one or more containers
- `dkP` Unpause all processes within one or more containers
- `dkpl` Pull an image or a repository from a registry
- `dkph` Push an image or a repository to a registry
- `dkps` List containers
- `dkpsa` List all containers (default lists just running)
- `dkr` Run a command in a new container
- `dkR` Run an interactive command in a new container and automatically remove the container when it exits
- `dkRe` like `dkR` and set entry point to `/bin/bash`
- `dkrm` Remove one or more containers
- `dkrmi` Remove one or more images
- `dkrmC` Clean up exited containers
- `dkrmI` Clean up dangling images
- `dkrmV` Clean up unused volumes ( Docker >= 1.9 )
- `dkrn` Rename a container
- `dks` Start one or more stopped containers
- `dkS` Restart a container
- `dkss` Display a live stream of container(s) resource usage statistics
- `dksv` Save one or more images to a tar archive (streamed to STDOUT by default)
- `dkt` Tag an image into a repository
- `dktop` Display the running processes of a container
- `dkup` Update configuration of one or more containers
- `dkV` Manage Docker volumes
- `dkv` Show the Docker version information
- `dkw` Block until a container stops, then print its exit code
- `dkx` Stop a running container

#### container (C)

- `dkC` Manage containers
- `dkCa` Attach to a running container
- `dkCcp` Copy files/folders between a container and the local filesystem
- `dkCd` Inspect changes on a container's filesystem
- `dkCe` Run a command in a running container
- `dkCin` Display detailed information on one or more containers
- `dkCk` Kill one or more running containers
- `dkCl` Fetch the logs of a container
- `dkCls` List containers
- `dkCp` Pause all processes within one or more containers
- `dkCpr` Remove all stopped containers
- `dkCrn` Rename a container
- `dkCS` Restart one or more containers
- `dkCrm` Remove one or more containers
- `dkCr` Run a command in a new container
- `dkCR` Run an interactive command in a new container and automatically remove the container when it exits
- `dkCRe` like `dkCR` and set entry point to `/bin/bash`
- `dkCs` Start one or more stopped containers
- `dkCss` Display a live stream of container(s) resource usage statistics
- `dkCx` Stop one or more running containers
- `dkCtop` Display the running processes of a container
- `dkCP` Unpause all processes within one or more containers
- `dkCup` Update configuration of one or more containers
- `dkCw` Block until one or more containers stop, then print their exit codes

#### image (I)

- `dkI` Manage images
- `dkIb` Build an image from a Dockerfile
- `dkIh` Show the history of an image
- `dkIim` Import the contents from a tarball to create a filesystem image
- `dkIin` Display detailed information on one or more images
- `dkIls` List images
- `dkIpr` Remove unused images
- `dkIpl` Pull an image or a repository from a registry
- `dkIph` Push an image or a repository to a registry
- `dkIrm` Remove one or more images
- `dkIsv` Save one or more images to a tar archive (streamed to STDOUT by default)
- `dkIt` Tag an image into a repository

#### volume (V)

- `dkV` Manage volumes
- `dkVin` Display detailed information on one or more volumes
- `dkVls` List volumes
- `dkVpr` Remove all unused volumes
- `dkVrm` Remove one or more volumes

#### network (N)

- `dkN` Manage networks
- `dkNs` Connect a container to a network
- `dkNx` Disconnects a container from a network
- `dkNin` Displays detailed information on a network
- `dkNls` Lists all the networks created by the user
- `dkNpr` Remove all unused networks
- `dkNrm` Deletes one or more networks

#### system (Y)

- `dkY` Manage Docker
- `dkYdf` Show docker filesystem usage
- `dkYpr` Remove unused data

#### stack (K)

- `dkK` Manage Docker stacks
- `dkKls` List stacks
- `dkKps` List the tasks in the stack
- `dkKrm` Remove the stack

#### swarm (W)

- `dkW` Manage Docker Swarm

### Docker Machine

- `dkm` is short for `docker-machine`
- `dkma` Get or set the active machine
- `dkmcp` Copy files between machines
- `dkmd` Set up the default machine ; alowing you to use `dkme` without arguments
- `dkme` Set up the environment for the Docker client (eg: `dkme staging` to toggle to staging)
- `dkmin` Inspect information about a machine
- `dkmip` Get the IP address of a machine
- `dkmk` Kill a machine
- `dkmls` List machines
- `dkmpr` Re-provision existing machines
- `dkmps` is alias for `dkmls`
- `dkmrg` Regenerate TLS Certificates for a machine
- `dkmrm` Remove a machine
- `dkms` Start a machine
- `dkmsh` Log into or run a command on a machine with SSH
- `dkmst` Get the status of a machine
- `dkmS` Restart a machine
- `dkmu` Get the URL of a machine
- `dkmup` Upgrade a machine to the latest version of Docker
- `dkmV` Show the Docker Machine version or a machine docker version
- `dkmx` Stop a machine

### Docker Compose

- `dkc` is short for `docker-compose`
- `dkcb` Build or rebuild services
- `dkcB` Build or rebuild services and do not use cache when building the image
- `dkcd` Stop and remove containers, networks, images, and volumes
- `dkce` Execute a command in a running container
- `dkck` Kill containers
- `dkcl` View output from containers
- `dkcls` is alias for `dkcps`
- `dkcp` Pause services
- `dkcP` Unpause services
- `dkcpl` Pull service images
- `dkcph` Push service images
- `dkcps` List containers
- `dkcr` Run a one-off command
- `dkcR` Run a one-off command and remove container after run.
- `dkcrm` Remove stopped containers
- `dkcs` Start services
- `dkcsc` Set number of containers for a service
- `dkcS` Restart services
- `dkcu` Create and start containers
- `dkcU` Create and start containers in detached mode: Run containers in the background, print new container names
- `dkcV` Show the Docker-Compose version information
- `dkcx` Stop services

## Acknowledgements

This module is a copy of [akarzim/zsh-docker-aliases][5] by [François Vantomme][6] (MIT License).

Completion for [docker][7] [docker-compose][8] [docker-machine][9]

[1]: https://www.docker.com/
[2]: https://docs.docker.com/compose/
[3]: https://docs.docker.com/machine/

[4]: https://github.com/docker/cli/commit/b10fb43048

[5]: https://github.com/akarzim/zsh-docker-aliases
[6]: https://github.com/akarzim

[7]: https://raw.githubusercontent.com/docker/cli/master/contrib/completion/zsh/_docker
[8]: https://raw.githubusercontent.com/docker/compose/1.29.2/contrib/completion/zsh/_docker-compose
[9]: https://github.com/leonhartX/docker-machine-zsh-completion

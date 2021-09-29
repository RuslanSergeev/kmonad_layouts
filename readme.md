# Keyboard layouts for the Keymonad 

This repo contains keyboards and layers definitions for
the keyboards I use. The definition files are intended
to be used with the KMonad service.

You can also try to execute just once:
```shell
source monad.sh [desired_layout.kbd]
```

# Available keyboards configs:

- Microsoft sculpt ergonomic split [keyboard](sculpt.kbd)  
- Dell universall 100 percent [keyboard](dell_ansi_100.kbd)
- sculpt 2 layers simplified layout [keyboard](sculpt_2layers.kbd)
- asus 2 layers simplified layout [keyboard](asus_2layers.kbd)

# Installing KMonad:

Clone the latest kmonad version:
```git clone
git clone https://github.com/kmonad/kmonad.git
```

After clonning the KMonad, perform the compiling with docker:
```shell
# Build the Docker image which will contain the binary.
docker build -t kmonad-builder .

# Spin up an ephemeral Docker container from the built image, to just copy the
# built binary to the host's current directory bind-mounted inside the
# container at /host/.
docker run --rm -it -v ${PWD}:/host/ kmonad-builder bash -c 'cp -vp /root/.local/bin/kmonad /host/'

# Clean up build image, since it is no longer needed.
docker rmi kmonad-builder
```



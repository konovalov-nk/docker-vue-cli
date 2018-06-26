# About

This container will have the items necessary to run the @vue/cli (version 3.x).

# Using this container

In your .bashrc, .zshrc, or similar file include aliases for the
following commands:

```
alias vue='docker run -it --rm -v "$PWD":"$PWD" -w "$PWD"  -u "$(id -u)" konovalovnk/vue-cli-latest vue'
```

On Mac OS X you'll have to remove `-u "$(id -u)"` part:

```
alias vue='docker run -it --rm -v "$PWD":"$PWD" -w "$PWD" konovalovnk/vue-cli-latest vue'
```


Using this via docker-compose:

```
version: '2'
services:
  web:
    image: konovalovnk/vue-cli-latest
    command: npm run dev
    volumes:
      - .:/code
    ports:
      - "8080:8080"
```

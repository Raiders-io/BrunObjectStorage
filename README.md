# BrunObjectStorage

## Commands

### Setup commands

Define the port of the API with a var, and with a command, you can change all the URL at once.

```sh
export PORT=3334
```

```sh
sed -i -E "s#(http://127\.0\.0\.1:)[^/]+(/.*)#\1${PORT}\2#" *
```

To use a Token for all the requests that needs them, you need to use :

```sh
export API_TOKEN=placeholder
```

```sh
sed -i -E "s|(Bearer ).*|\1${API_TOKEN}|" ./**/*.bru
```

### Reset/Revert to default

Please avoid publishing secrets as tokens, files (even paths), identities or anything else.

To revert the command and not publish secrets, you can revert with this command :

```sh
sed -i -E "s|(Bearer ).*|\1[token]|" ./**/*.bru
```

To remove files from forms :

```sh
sed -i -E "s|(files\[\]: ).*|\1|" Objects/createObject.bru
```

# BrunObjectStorage

## Commands

### Setup commands

The project uses `ENV` vars to create the requests.

To use a Token for all the requests that needs them, you need to use :

1. Signup/Login and copy the token in `data{}`.
2. Open the environment of `Bruno`/`WebDocumentation` of **opencollection**.
3. Paste the token in the value section.

### Reset/Revert to default

Please avoid publishing secrets as tokens, files (even paths), identities or anything else.

You can use the following command to reset everything in this repository :

```sh
chmod +x ./reset.sh
./reset.sh
```

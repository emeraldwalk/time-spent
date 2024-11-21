## Release Process

### Setup

Update version in `package.json`

### Verification

1. Verify contents to publish `vsce ls`
1. Package local `.vsix` for testing `npx vsce package`

### Publishing

#### Pre-Release

Run the following script to do a pre-release:

```sh
# Update pre-release version in command before running it
scripts/pre-release.sh 0.1.X
```

#### Release

```sh
vsce publish patch --allow-star-activation
git push
git push --tags
```

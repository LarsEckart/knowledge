# NodeJS

## npm

### Allow `npm install -g` without needing `sudo`

```
npm config set prefix $dir
chown -R lars $dir
```

### Change the default save prefix for all your projects

```
npm config set save-prefix ~
```

The tilde (~) is more conservative than what npm defaults to, the caret (^), when installing a new package with the --save or --save-dev flags. The tilde pins the dependency to the minor version, allowing patch releases to be installed with npm update.
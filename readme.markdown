# git-image-diff

git diff for images

# usage

```bash
git diff # show using picture-tube
OPEN=true git diff # show using default image program
```

# install

1. `npm install picture-tube -g`
2. `convert` needs to be in your path installed by [ImageMagick][imagemagick].
3. `cp image-diff /usr/local/bin`
4. Change `attributes` and `.gitconfig` as below

```bash

~/.config/git/attributes
*.png  diff=image-diff
*.jpg  diff=image-diff
*.jpeg diff=image-diff
*.gif  diff=image-diff

~/.gitconfig
[diff "image-diff"]
  command = /usr/local/bin/image-diff
```

# license

MIT

[imagemagick]: http://www.imagemagick.org
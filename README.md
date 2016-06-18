# Minimal Boilerplate for HarpJS + Surge.sh with Git Hooks

**For a more opinionated, SkilStak-centric boilerplate consider [html5-harp-boilerplate][].**

Jade + Stylus + JavaScript + `harp compile` and `surge www` hooks to
get you started out right with a free static site without the quirks of
gh-pages relative image links and other problems.

1. Fork or copy
2. `ln -s ../../_pre-commit .git/hooks/pre-commit`
3. Change CNAME to your preferred domain (`<you>.surge.sh`)
4. Edit and add files
5. `git commit` etc. or ...

You could add a `save` script like the following to your bin:

```sh

#!/bin/sh
comment=save
[ ! -z "$*" ] && comment="$*"
git pull
git add -A .
git commit -a -m "$comment"
git push
```

... which will trigger the `.git/hooks/pre-commit` to `harp compile` and
`surge www` the site.

[html5-harp-boilerplate]: https://github.com/skilstak/html5-harp-boilerplate

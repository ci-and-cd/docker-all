# docker-all

All docker modules managed by git submodule

Created by
```bash
find . -name '.git' | grep docker- | grep -v docker-all | awk -F/ '{print $2}' | sort | xargs -i echo git submodule add git@github.com:ci-and-cd/{}.git {}
```

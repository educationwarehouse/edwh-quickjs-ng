# edwh-quickjs-ng

```bash
git clone --recurse-submodules  git@github.com:educationwarehouse/edwh-quickjs-ng.git
cd edwh-quickjs-ng/
git -C upstream-quickjs fetch
git -C upstream-quickjs checkout v0.14.0
# edit version in pyproject.toml
git add upstream-quickjs
git add pyproject.toml
git commit -m "bump upstream-quickjs to v0.14.0"
make install
(make test)
make build
```

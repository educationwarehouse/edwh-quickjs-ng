# edwh-quickjs-ng

```bash
git clone --recurse-submodules git@github.com:educationwarehouse/edwh-quickjs-ng.git
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

Note that `make publish` would only publish the wheel for your local system.
It's better to use the github action.
Releases are published automatically by GitHub Actions when you push a version
tag.

```bash
git tag v0.14.0.1
git push
git push --tags
```

This triggers `.github/workflows/build.yml`, which builds cross-platform wheels
and sdist, then publishes to PyPI.

No manual workflow dispatch or local `uv publish` is needed for normal releases.

# Pack builder

Build a container image using `pack`.

Default configuration:

- Heroku 24 builder
- Heroku/Python pack
- Heroku/Procfile pack
- Infrabits/envvar pack

## Example Usage

```
  build-container:
    runs-on: ubuntu-latest
    steps:
      - uses: infrabits/ci-pack@main
        with:
          image: ghcr.io/${{ github.repository }}:${{ github.sha }}
          runtime_release: ${{ github.sha }}
```

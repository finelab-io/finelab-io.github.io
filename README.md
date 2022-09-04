
# developer.finetech.dk
## Get started 
### Create Github Pages with Jekyll and chirpy

See video by Techno Tim to setup: https://youtu.be/F8iOU1ci19Q

``` bash
bundle

docker run \
  -it \
  --rm \
  --volume="$PWD:/srv/jekyll" \
  -p 4000:4000 jekyll/jekyll \
  jekyll serve
```

### Create API documentation with Widdershins
See getting started here: https://github.com/Mermade/widdershins

``` bash 
npm install -g widdershins

node widdershins \
--search false \
--language_tabs 'http:Http' 'javascript:Javascript' \
--summary \
https://raw.githubusercontent.com/finetech-dk/specs/main/sales/order/order-api.yaml \
-o _posts/order-api-2022-09-04.md

```
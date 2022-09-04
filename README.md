
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


widdershins --search false --language_tabs 'http:Http' --summary https://raw.githubusercontent.com/finetech-dk/specs/main/sales/order/order-api.yaml -o _posts/2022-09-04-order-api.md

widdershins --search false --language_tabs 'http:Http' --summary https://raw.githubusercontent.com/finetech-dk/specs/main/sales/order/order-service.yaml -o _posts/2022-09-04-order-service.md



```
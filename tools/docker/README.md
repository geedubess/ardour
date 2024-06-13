Builds in a docker container.

# Build non-interactively:
docker compose build
docker compose run --rm app sh -c '/ardour/waf configure \
        --freedesktop \
        --noconfirm \
        --libjack=weak \
        --no-phone-home \
        --use-external-libs \
        --cxx11 \
        --ptformat \
        --with-backends=jack,dummy \
        --prefix=/usr/local/ \
        --lv2dir=/usr/local/lib/lv2 \
        --configdir=/usr/local/etc/ \
        && /ardour/waf build'

# Interactively build:
docker compose run --rm app bash
ubuntu@a855845e4f7e:/ardour$ ...

# Play with deps while interactive shell is open:
docker compose exec -it --user root app bash

# Interactively build and play with deps:
docker compose run --user root --rm app bash
root@d173236724cd:/build# apt install foo && su - ubuntu -c /ardour/waf ...

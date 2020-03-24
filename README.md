# Nginx with lua-resty-openidc

This image provides an installation of nginx, with openresty and the additional module `lua-resty-openidc` which provides OpenID Connect functionalities.

The `nginx.conf` file is the one provided by openresty, which has the directive `include /etc/nginx/conf.d/*.conf;` so all nginx configurations in that directory will be included.
The default virtual host configuration has the original OpenResty configuration and is copied to /etc/nginx/conf.d/default.conf.

You can override that default.conf directly or volume bind-mount the /etc/nginx/conf.d directory to your own set of configurations:
```sh
docker run -v /my/custom/conf.d:/etc/nginx/conf.d moxoff/lua-resty-openidc
```


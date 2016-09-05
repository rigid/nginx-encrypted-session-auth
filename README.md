= nginx encrypted session auth =

This is an example for nginx-only auth, using a HTTP POST form.
It includes login/logout and per-user root directories.

Prerequisites:
* nginx

and as modules:
* https://github.com/openresty/set-misc-nginx-module
* https://github.com/openresty/encrypted-session-nginx-module
* https://github.com/calio/form-input-nginx-module
(which are currently not included with nginx)

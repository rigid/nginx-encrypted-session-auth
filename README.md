# nginx encrypted session auth

This is an example for nginx-only auth, using a HTTP POST login form without CGI.
It covers login/logout/failed login and per-user directories.

## Prerequisites:
* nginx

and nginx modules:
* https://github.com/openresty/set-misc-nginx-module
* https://github.com/openresty/encrypted-session-nginx-module
* https://github.com/calio/form-input-nginx-module
(which are currently not included with nginx)

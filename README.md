# nginx encrypted session auth

This is an example for nginx authentication using a HTTP POST login form without CGI.
It covers login/logout/failed login and per-user directories.

## Prerequisites:
* nginx
* nginx modules:
 * https://github.com/openresty/set-misc-nginx-module
 * https://github.com/openresty/encrypted-session-nginx-module
 * https://github.com/calio/form-input-nginx-module
(which are currently not included with nginx)

# How it works:
- auth_request is used to authenticate against another server (which uses auth_basic in itself for the demo)
- The necessary headers are set for the auth_request (username, password) and taken from an encrypted cookie.
- The cookie is created in the target of a POST login form
  - if the cookie isn't present, login.html is shown
  - if the cookie is already present (but authentication failed), login-failure.html is shown
  - if the cookie is present and authentication suceeds, the users index.html is shown

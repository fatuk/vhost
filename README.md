# vhost
Script for creating virtual hosts for apache

## Installing:

Just place this script to `~/bin`.
And it will be available in terminal with `vhost`.
Check it out `vhost -h`.

## Available options:

| option               | description                                                                        |
| :------------------- | :------                                                                            |
| `-h`                 | help screen                                                                        |
| `-pub`               | to create the webhost root in ~/www/name/public/                                   |
| `-url`               | to specify a local address, default is http://name.loc                             |
| `-rm`                | to remove a previously created vhost, see examples                                 |
| `-d`                 | to specify the webroot directory location, default is in ~/www (NO TRAILING SLASH) |
| `-email`             | to specify the email of the administrator in the virtual host file                 |
| `-l`                 | to list the current virtual hosts                                                  |


## Examples:

| command                                                     | description                                                                                                                          |
| :----------                                                 | :------                                                                                                                              |
| `vhost mysite`                                              | this will create a new apache2 vhost named mysite with a webroot of `~/www/mysite/` reachable at `http://mysite.loc `                |
| `vhost -pub mysite`                                         | this will create a new apache2 vhost named mysite with a webroot of `~/www/mysite/public/` reachable at `http://mysite.loc`          |
| `vhost -d ~/sites/mysite/myroot -url dev.mysite.dev mysite` | this will create a new apache2 vhost named mysite with a webroot of `~/sites/mysite/myroot` reachable at `http://dev.mysite.dev`     |
| `vhost -rm mysite.loc mysite`                               | this will remove the apache2 vhost named mysite and remove the mysite.loc entry from the `/etc/hosts` file. Be sure to specify boths |


## IMPORTANT Notes:

1. You need **git** setup to grab the template file if you do not have it already.
2. You need to make sure you do not have a vhost called **'template'** or that it is the one from this gist: https://gist.github.com/f3c929e9d7b2bbb96d9a
3. Check your version of **sed**, you need to make sure -i works. GNU sed is suggested.

## Thanks

This is my fork of [gistwebdev](https://gist.github.com/gistwebdev)

* [vhost](https://gist.github.com/gistwebdev/5666279)
* [template](https://gist.github.com/gistwebdev/5640113)


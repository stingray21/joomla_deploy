# Deployment of Joomla extensions


## Links

- https://docs.joomla.org/Deploying_an_Update_Server

- https://github.com/joomla/joomla-cms/blob/staging/cli/update_cron.php

### Script

Create a new plain text file and paste that [code](https://raw.githubusercontent.com/akeeba/vagrant/master/assets/joomla/install-joomla-extension.php) in it. 
Save it as install-joomla-extension.php in your Joomla! site's cli directory. 
(The name is not important, the location (cli directory) is.)

Now you can call it like this:

```
cd /path/to/site/cli php ./install-joomla-extension.php --package=/where/is/your/extension.zip
```

The script returns one of the following exit statuses:

    0. The extension was installed successfully.
    1. The package file was not found.
    3. The package file could not be extracted.
    250. The extension could not be installed.


​	
You can copy this file to your site's cli directory and install extensions and extension updates any time you want.

- https://www.dionysopoulos.me/installing-joomla-extensions-from-the-command-line/
- https://stackoverflow.com/questions/41697091/how-to-install-joomla-extension-by-command
- https://github.com/akeeba/vagrant/blob/master/assets/joomla/install-joomla-extension.php


### Joomla 4 has better CLi support

- https://community.joomla.org/gsoc-2018/bringing-cli-update-to-joomla.html
- https://github.com/joomla/joomla-cms/blob/4.0-dev/cli/joomla.php
- https://github.com/joomla-projects/gsoc18_cli_update/pull/11

## Git deploy

- https://gist.github.com/noelboss/3fe13927025b89757f8fb12e9066f2fa

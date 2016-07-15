# Build

__Windows users, NB:__ ensure that you have Vagrant version >= 1.8.2 https://www.vagrantup.com/downloads.html

* From a clean location on your workstation, `git clone --recursive https://github.com/lsulibraries/ldl-dev`
* `cd ldl-dev`
* `vagrant up`
* once the provisioner completes, find the main site at http://localhost:8000
* for a more realistic environment, add the lines below to your system's `hosts` file: https://support.rackspace.com/how-to/modify-your-hosts-file/
  * with this done, you should be able to navigate to subsites http://hnoc.library.local:8000, http://ldl.library.local:8000, etc


~~~

127.0.0.1         hnoc.library.local
127.0.0.1         latech.library.local
127.0.0.1         loyno.library.local
127.0.0.1         lsm.library.local
127.0.0.1         lsu.library.local
127.0.0.1         lsuhsc.library.local
127.0.0.1         lsuhscs.library.local
127.0.0.1         mcneese.library.local
127.0.0.1         nicholls.library.local
127.0.0.1         state.library.local
127.0.0.1         subr.library.local
127.0.0.1         tahil.library.local
127.0.0.1         tulane.library.local
127.0.0.1         ull.library.local
127.0.0.1         ulm.library.local
127.0.0.1         uno.library.local
127.0.0.1         ldl.library.local

~~~

# IDE

## Using NetBeans

* `New Project`
* choose `PHP > PHP Application with Existing Sources`; `Next`
* Set `Sources Folder` to `<Path to this cloned repo>/wwwroot/ldl`; `Next`
* Set `Project URL` to `http://ldl.library.local:8000`, assuming that you have updated your `hosts` file; `Next`
* `Finish` the project setup; you should now find the project at the address given in the preceding step.

### Xdebug

First, we will need to edit the server-side xdebug config to listen for your workstation's IP.

* `vagrant ssh`
* `sudo su`
* edit `/etc/php5/apache2/conf.d/20-xdebug.ini` in your preferred editor
* for the key `xdebug.remote_host`, ensure that it's value is your workstation IP.
* once done, restart apache2 to pick up the new config


Back in NetBeans, 

* In `Tools > Options > PHP > Debugging`, ensure:
  * `Debugger Port: 9000`
  * `Stop at First Line:` checked

You should now be able to Debug the project with Ctrl-F5; if all is well, NetBeans will stop of the first line of the app which will be highlighted in green...

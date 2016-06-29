# Build

__Windows users, NB:__ ensure that you have Vagrant version >= 1.8.2 https://www.vagrantup.com/downloads.html

* From a clean location on your workstation, `git clone --recursive https://github.com/lsulibraries/ldl-dev`
* `cd ldl-dev`
* `vagrant up`
* once the provisioner completes, find the main site at http://localhost:8000
* for a more realistic environment, add the lines below to your system's `hosts` file: https://support.rackspace.com/how-to/modify-your-hosts-file/
  * with this done, you should be able to navigate to subsites http://hnoc.library.local, http://ldl.library.local, etc


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
GalaxyP - ProteoWizard msconvert
================================

* Home: <https://bitbucket.org/galaxyp/msconvert>
* Galaxy Tool Shed: <http://toolshed.g2.bx.psu.edu/view/galaxyp/msconvert>
* Tool ID: `msconvert`
* Tool Type: `default`


Description
-----------

msconvert from ProteoWizard.

See:

* <http://proteowizard.sourceforge.net/>
* <http://proteowizard.sourceforge.net/tools/msconvert.html>


Warning Notice
--------------

This repository requires a custom modification to Galaxy. It should be considered unsupported by the GalaxyP community until this notice is removed.

```
MULTIFILE_EXTENSION_PREFIX = "m:"

msconvert.xml
10:    #if $ext.startswith("m:")
11:    #set $ext = $ext[len("m:"):]

msconvert_raw.xml
13:    #if $ext.startswith("m:")
14:    #set $ext = $ext[len("m:"):]
```


Installing
----------

Due to potential difficulties installing ProteoWizard with vendor library support, tools for interacting with vendor types are seperated out into their own wrappers. Galaxy is generally deployed under Linux, but vendor support in ProteoWizard requires .NET 4.0. There are at least two ways to get this to work:

* Galaxy jobs may be configured to submit to a Windows host with ProteoWizard installed using the [LWR](https://wiki.g2.bx.psu.edu/Admin/Config/LWR).

* ProteoWizard can be installed under Wine. Guidance on how to set this up and package such environments for cloud deployments can be found here: <https://github.com/jmchilton/proteomics-wine-env>


GalaxyP Community
-----------------

Current governing community policies for [GalaxyP](https://bitbucket.org/galaxyp/) and other information can be found at:

<https://bitbucket.org/galaxyp/galaxyp>


License
-------

Copyright (c) 2014 Regents of the University of Minnesota and Authors listed below.

To the extent possible under law, the author(s) have dedicated all copyright and related and neighboring rights to this software to the public domain worldwide. This software is distributed without any warranty.

You should have received a copy of the CC0 Public Domain Dedication along with this software. If not, see <https://creativecommons.org/publicdomain/zero/1.0/>.

You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission.


Contributing
------------

Contributions to this repository are reviewed through pull requests. If you would like your work acknowledged, please also add yourself to the Authors section. If your pull request is accepted, you will also be acknowledged in <https://bitbucket.org/galaxyp/galaxyp/CONTRIBUTORS.md> unless you opt-out.


Authors
-------

Authors and contributors:

* Björn Grüning
* Cody Wang
* Fred Sadler
* John Chilton <jmchilton@gmail.com>
* Minnesota Supercomputing Institute, Univeristy of Minnesota

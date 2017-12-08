Yocto vanilla x86 manifest
==================================

This repository contains a git-repo manifest vanilla [Yocto Linux](https://www.yoctoproject.org/) with 
supporting layers and extensions to create valid images for generic x86_64 (intel core-i7) targets.

Installing Yocto Vanilla
------------------------------

To download Yocto manifest, you need the repo tool.

1. Download repo to a directory within your path and add execution permissions.

```
$ sudo curl -o /usr/local/bin/repo http://commondatastorage.googleapis.com/git-repo-downloads/repo
$ sudo chmod a+x /usr/local/bin/repo
```

2. Create an installation folder with user write permissions; for example, /opt/yocto. Navigate to that folder:

```
$ sudo install -o <your-user> -g <your-group> -d /opt/yocto
$ cd /opt/yocto
```

Note: You can get your primary user and group using the id command.

3. Use repo to download Yocto and the necessary layer extensions.

```
$ repo init -u https://github.com/exactassembly/yocto-repo.git -b krogoth
$ repo sync -j4 --no-repo-verify
```

License
-------
Copyright 2017, Exact Assembly, LLC

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

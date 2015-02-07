ContentTranslation is a tool that allows editors to translate pages from
one language to another with the help of machine translation and other
translation tools.

This is deployment repository of server component of ContentTranslation.

Layout
------
* debian - Debian directory, which can be use to build cxserver package.

* node_modules - node.js dependencies, updated with ``npm install``.

* src - cxserver js code as submodule.

* package.json - symlink to cxserver/package.json file.

How to
------

Update
======
To update node_modules:

```
npm install
```

To update src to latest cxserver master:

```
git submodule -q foreach git pull -q origin master
```

If checking out first time, do:

```
git submodule init
```

```
git submodule update --init --recursive
```

Submit changes
==============
1. Do changes you want to add (either node_modules or cxserver src)

2. Find what has been change in cxserver using,

```
git log --oneline --decorate --color --graph -n10
```

3. Describe changes in commit message.

4. Submit change in Gerrit.

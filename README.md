Generate HTML CLI Tools
=======================

**DISCLAIMER**: This program is not meant to be used by anyone at anytime for
any reason. There is no warranty and no reason anyone should even think this
is a good idea to run.

Use bash to generate some HTML.

Example
-------

Simple tag:

```
$ p "hello $USER"
<p>
	hello dave
</p>
```

Pipe tags:

```
$ p "hello $USER" | body | html
<!doctype html>
<html>
	<body>
		<p>
			hello dave
		</p>
	</body>
</html>
```

Pipe multiple tags:

```
$ cat \
> <(title 'My Website' | head) \
> <(p "hello $USER" | body) \
> | html
<!doctype html>
<html>
	<title>
		My Website
	</title>
	<body>
		<p>
			hello dave
		</p>
	</body>
</html>
```

Usage
-----

Clone the repo and put the tools in your `PATH`:

```
git clone git@github.com:bahamas10/bash-html.git
cd bash-html
PATH=$PWD/bin:$PATH
```

Now you will have access to every commend in the [`./bin`](/bin) directory.

License
-------

MIT License

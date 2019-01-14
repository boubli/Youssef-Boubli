---
layout: article
title: "Creating standalone Mac OS X applications with Python and py2app"
date: 2017-27-12 19:45:00+0200
coverPhoto: http://me.seekingqed.com/static/img/python2mac/python2mac.png
---

In this tutorial we’ll be using py2app to create a standalone OSX application from a Python 2 or 3 source code with a simple Tkinter user interface.

"py2app is a Python setuptools command which will allow you to make standalone application bundles and plugins from Python scripts. py2app is similar in purpose and design to py2exe for Windows."

```cmd
	# Create a custom directory
	$ mkdir MyApp
	$ cd MyApp

	# Use virtualenv to create an isolated environment
	$ virtualenv venv
	$ . venv/bin/activate
```

Now create a very simple Tkinter app with the filename `MyApp.py`:

```cmd
	import sys
if sys.version_info < (3, 0):
    # Python 2
    import Tkinter as tk
else:
    # Python 3
    import tkinter as tk
root = tk.Tk()
root.title("Sandwich")
tk.Button(root, text="Make me a Sandwich").pack()
tk.mainloop()
```






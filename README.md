# Python OMXPlayer wrapper

[![Documentation
Status](https://readthedocs.org/projects/python-omxplayer-wrapper/badge/?version=latest)](https://readthedocs.org/projects/python-omxplayer-wrapper/?badge=latest)
[![Build
Status](https://travis-ci.org/willprice/python-omxplayer-wrapper.svg)](https://travis-ci.org/willprice/python-omxplayer-wrapper)


> Control OMXPlayer from Python on the Raspberry Pi.

## adjustments for Python3 by schlizbaeda 
bus_finder.py: cast/convert return value of command "filter" from type "iterator" to type "list"
player.py: DON'T cast/convert return value of command "self._get_properties_interface().Duration()" to type "long"

## Install
For someone who just wants to use the package:
```shell
$ python setup.py install
```

If you're feeling helpful, and decide to help develop the package:
```shell
$ python setup.py develop
```
This will install via symlinks so that you can continue to work on it locally
but import it from other python packages

## Hello world
```python
from omxplayer import OMXPlayer
from time import sleep

# This will start an `omxplayer` process, this might 
# fail the first time you run it, currently in the 
# process of fixing this though.
player = OMXPlayer('path/to/file.mp4')

# The player will initially be paused

player.play()
sleep(5)
player.pause()

# Kill the `omxplayer` process gracefully.
player.quit()
```

## Docs
You can read the docs here:
[python-omxplayer-wrapper.rtfd.org](http://python-omxplayer-wrapper.rtfd.org)

# beets-moveall-artifacts

## Installation

Clone this repository and then `python setup.py` should do the trick.
Note that, as of this writing, the moveall plug-in in this package
requires Beets 1.2.2 (currently unreleased) or later.  I'm running
Beets from Git right now.

Once you've installed this package, to use one or both of these
plug-ins you'll need to [configure them in Beets][enable-plugins].

[enable-plugins]: http://beets.readthedocs.io/en/latest/plugins/index.html#using-plugins

## Plugin: moveall

If you activate this plug-in, any time you move every music file out
of one directory and into another with `beet mv`, any files in the old
directory that are not known to Beets will be moved to the new
directory as well.  This is useful when you have files like EAC log
files or README.TXT files for an album that should get moved along
with that album.

If you move files from a single directory into multiple other
directories, this plug-in will take no action; non-Beets files in the
source directory will be left where they are.

If this plug-in moves all of the files out of your old directory, it
will automatically try to remove the old directory as well.  Again,
this is useful when you're moving a complete album in its own
directory, which also contains additional non-music files.

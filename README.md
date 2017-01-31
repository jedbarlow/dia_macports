Portfile for modded Dia
=======================

This project contains a MacPorts Portfile for my modded version of Dia, which implements an option
for smoother scrolling.

Instructions
------------

Clone this repo to your local filesystem and add the following line, with the path modified
appropriately, to the top of the `sources.conf` file (which is probably located at
`/opt/local/etc/macports/sources.conf` if you have the default installation of MacPorts).  It is
important that this line comes before other port tree sources, since MacPorts will use the first
definition of a port that it finds. 

```
file:///ABSOLUTE/PATH/dia_macports
```

Then run the following to install Dia.

```bash
sudo port install dia
```

Then a `Scroll step percentage of view dimension` option will be available under
`File`->`Preferences`->`User Interface`.  Setting this field to something like `0.65` makes
scrolling a lot better if you're using a trackpad on a laptop.

Keep in mind that you'll need to install XQuartz for Dia to run, and one way to launch Dia is to
open up a terminal through XQuartz and just enter `dia` from the command line there.

=================
Command framework
=================

Squirtgun includes a flexible command framework, taking design cues from Mojang's Brigadier. It aims to be declarative wherever possible to make creating complex command chains easy.

#########
Key Terms
#########

+++++++
Command
+++++++

There is no such thing as a command.

+++++++++++++
Command Chain
+++++++++++++
* A command chain is a list of command nodes.
* Whereas a framework designed by someone with an element of sanity might use a tree, the command chain is entirely implicit. You probably could draw a tree from your command nodes, but why would you do that?

++++++++++++
Command Node
++++++++++++
* A command node is a single element in a command, that does a thing when executed.
* It may expose arguments. 
* It may have a child node - when this is used is explained below.
* Command nodes can not be tab-completed, however its arguments can.

++++++++
Argument
++++++++
* An argument is some kind of value that a command node expects input for.
* It is *not* necessarily a single space-delimited string element as most low-level frameworks such as Bukkit provide. It may consume more elements
* An argument can be tab-completed.

## Stack Environment

Originally published: 2012-05-29 14:47:23
Last updated: 2012-05-29 14:53:25
Author: Alfe 

The environment variables of processes get inherited by their children who can modify them and pass them on to their children.  The tree of processes is similar to the call tree of a running Python process, but a similar mechanism like the environment variables is missing.  I'm offering a solution for this; each stack frame takes the place of a process, hence I call it StackEnv.  It comes in handy if you want to pass information from one frame to a frame far below without patching all the calls in between to pass the data (which might belong to a framework you don't want to change).
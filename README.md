UPDATE 2021:
============

Newer versions of UE have some work to allow setting the Shader Compiler Priority.

The required setting was not in the BaseEngine.ini file for the latest version of UE I had, but you can simply add the follow key to the ini.

Find the BaseEngine.ini file, in there, find the [DevOptions.Shaders] section, then add this line:

WorkerProcessPriority=1


====================================================




Why?
====


I've been trying to use Unreal Engine on my slightly inadequate computer. CPU G3258 a bit lacking the multicore department!

One thing I have really noticed is how slow Unreal's shader compiler is on my environment. It can take upto two minutes to compile the shader even with very simple changes to the material.

For some reason unreal launches the compiler at 'below normal' priority. Which may be fine for anyone with cores to spare but is not that great for me.

This exe, keeps looking for the process, checks its priority is not at Normal, and changes it if it isnt.

Just launch it as you start Unreal, it will keep monitoring until you *ctrl-c* out of it.



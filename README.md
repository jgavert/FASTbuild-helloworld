# FASTbuild-helloworld
A sample way to define a FASTbuild script to build a library and link that to a another library to create executable.
You can find more information about FASTbuild here http://www.fastbuild.org/

# Compiling Prequisites
Check the fbuild.bff beginning for the hardcoded directory paths.
You can probably notice soon that this project is only for x64 with newest visual studio 2015 ctp6. Tested on win8.1.
There were some libucrt.lib(Universal CRT) changes which are applied to this sample project.
Also you should have latest fbuild 0.80 or greater also. Easiest way is to copy the FBuild.exe to this folder.

# Visual studio project files
In windows Cmd "fbuild.exe proj"
Check out how "proj" is defined in the fbuild.bff file to see more. 

# Compiling
Just run fbuild.exe without specifying anything.
You could also say "fbuild all" which basically does the same thing.

# Notes
Most of the time went to figuring out what kind of switches I need to feed the msvc compiler.
To get the clearest picture on what I have done, you should compre the FASTbuilds sources fbuild.bff to this projects.
I basically stripped additional platforms and compilers away. There were some changes to support vs2015 so that took about 2 hours.
All in all it took about 6 hours to get it working by imitating the FASTbuilds own files.

# Motivation
I used cmake before, but I didn't find a way to easily specify this kind of project structure. I found cmake to be confusing.
Biggest motivation was that it has linux support now so I kind of wanted to do a hello world to see how complex this is.
Added benefit of course is the advertised build speeds that I have yet to compare. But as far as I'm concerned, this sample is, more or less, final.
If you want to add more platforms/compilers, I highly recommend on downloading the FASTbuild source and look its configs.
They were good tutorial material and provide a nice base structure on which to build on. Without that base, this wouldn't have been so trivial.

I might have missed something, but hope this helps to get in speed with FASTbuild.

This repository was created when FASTbuild 0.80 was released. There most likely will not be updates to this regardless if FASTbuild changes and this repository gets broken.
There is a chance that I might fix this to correspond vc2015 when it gets released.
I'm conflicted about accepting patches, rather do your own repository!

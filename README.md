# NetBeans2
Trying to get net beans to use a remote repository on github. I think I finally got one step working - namely creating a local project and shoving it to a remote repository.

You need to
1. create a project
2. use Team>Git>Initialize Repository  // so git tracks locally
3. Team>Comit // so that git knows that you want to keep the local files
4. Create a Repository on gitHub and copy the HTTPS location that you get
5. use Team>Remote>Push // fill in copied HTTPS link, git user name and password

and in theory it is there. This only took 2 days and a couple tutorials. Now we see if someone else can get at the repository.

--
Indeed, one can get to this repository from another machine however there is a gotcha: When a brand new freshly installed netbeans clones the remote repository it does in fact appear to get all the files but the code will not build and run on the new machine. Why? Apparently somewhere in my system that was first used to build this repository I had some configuration setup, perhaps to force my system to use a particular build of the java compiler. That configuration setting appears to have been uploaded along with everything else (just as is should) and when you try to run on a new machine it tells you "You are missing some configuration setting". It doesn't tell you what it is, or where it is set, or suggest a fix or anything that is particularly useful. I don't know what I need to change on my machine so that I can upload a vanilla configuration so that you can get it without screwing around. 

I did actually manage to get it working on the new build, though I did is several days ago and don't recall exactly what I did. I found a menu item in the inpenetrable forest that allows one to build custom configurations and I told it to build a new one that does absolutely nothing different from the default configuration but that has the same name as the one that I was told was missing. With that fix apparently netbeans can find the congifuration that it was looking for and things appear to work. Caveat Emptor!

# WORKING!
Unofficial alma linux live images



livemedia/livecd images/ kickstarts  and rpms to rebuild your own. 'respin'




Orginally when I started to created a new spin from alma, rebuilding a live image failed for me:
So I set out quickly to see wut the problem was.
I soon saw, that ALMA engineers had just used the default version from upstream (pure 1:1) of anaconda with exception of logos/graphics. Doing so, left
the IBMHAT Subscriber network bits intact. Which is great for full RH emulation. However, I like to build live images so, I rebuild
the version from Springdale Linux for ALMA and fixed. Just upgrade the anaconda versions from alma with newer that doesnt include the code
for the RHSN network bits and your livemedia-creator ready.


If you try to rebuild a livemedia image from UPSTREAM IBMHAT proper using a clone OS such as alma with 1:1 anaconda bits, the following error will occur as expected. 

```
Anaconda fails with an error - "dasbus.error.DBusError: The RHSM DBus API is not available."
```

The version here rebuild came from springdale.


https://bugzilla.redhat.com/show_bug.cgi?id=1872902


I rebuilt anaconda with anaconda-live and included it in to be picked up the kickstart.
The iso image is in releases and below:


To create your own spin version you will need to rebuild anaconda and/or use the rpms I have here and update your kickstart to where you have them before you rebuild.


Note when building a minimal, if you really want to build a minmal it will have a text gui anaconda installer and still be fairly large unless you start trimming it in more detail. It is worth it to me to leave the gnome packages in for the install. You could easily build/respin a Xfce/Cinna/Sugar lightweight based EL8 desktop as default too for older hardware, but that is another project!


The repo here is what was used to create the live image. 

To reproduce your own live image with livemedia-creator you will need to set these up somewhere for your spin to use as well.
Update the ip and directory to your actual. You shouldnt need to run createrepo again, unless you just want to rebuild anaconda again too.


Related references in kickstart:
```
#This is done to add the anaconda-live
repo --name="Updates_AppStream" --baseurl=http://192.168.1.253/tmplive/
```

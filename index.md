

RPM distro Sysadmin working with Ubuntu
=======================================

I recently had to dive into some in-depth Ubuntu system admnistration, coming from  
working mostly on Redhat based systems. The first issue I ran into, was locating Ubuntu's  
version of the `/etc/sysconfig/network` scripts.  I needed to configure networking, and   
I couldn't determine what was managing the interfaces.  The server was running Ubuntu 22.04,  
and although I've used Ubuntu 20.4 for some time, it's mostly been on the desktop, or  
with minimal server configuring.  I'm documenting my journey here for future reference, I'll  
be updating this post as I progress.  


Networking
----------
## Interface config file location  
`/etc/network`  
`/etc/network/interfaces`  
Interfaces can be configured for Network Manager control or Manual Configuration in `/etc/network/interfaces`

### Discover interfaces  
`# nmcli g`

### Get connection details
`# nmcli c`

### Get device details
`# nmcli d`

### Delete a connection
`# nmcli c delete "Wired Connection 1"`

## Create a new connection
`# nmcli c e`
Short for `nmcli connection edit

## Print configurable parameters  
`nmcli> print ipv4`

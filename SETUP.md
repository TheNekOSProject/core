# Creating NekOS from scratch  
in this file we define the procedure to get a base we can start working on to develop the full NekOS distro  
NekOS development is contained within a VM and the host communicates with the container via the `neko-development-bridge`  

## Steps  
1) install a minimal debian base with no graphical servers but only contains (kernel, core utils, init, networking)  
2) make sure the VM is connected via a tunnel to the host  
3) install the `neko-development-bridge` on the container  
4) install the `neko-bridge-tools` on the host  

## The development bridge  
this bridge (available at the organization repos) deals with sideloading tools and files to the container  
it's also used to manage apt and services  

## search for mounted nfs files

showmount -e ip



## mount nfs
sudo mount -t nfs 10.10.13.134:/home /tmp/mount/ -nolock 
sudo mount -t nfs 10.10.13.134:shared_folder mount point -nolock 
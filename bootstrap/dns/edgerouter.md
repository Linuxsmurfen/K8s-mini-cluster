## Update DNS
Update the DNS to point to the ingress IP.
Login to the EdgeRouter and add a wildcard DNS entry. 

```
$ configure
# set service dns forwarding options 'address=/k8s.home.ip/192.168.x.x'
# commit
# save
# exit
```

Thanks to   
https://gist.github.com/plembo/6bb4491ebbfbce049c7efce0634d57f0   
https://jimangel.io/post/edgerouter-os-cli-cheatsheet/

# clean apache2 cache disk
Run the folowing command
```
systemctl stop apache-htcacheclean && systemctl stop apache2 && htcacheclean -v -p /var/cache/apache2/mod_cache_disk -l1024M -L1k && systemctl restart apache-htcacheclean && systemctl restart apache2 && systemctl restart apache-htcacheclean
```
  This will ensure the cache is cleared and the maximum cache size  is set to 1GB 
  
  Ensure that `/var/cache/apache2/mod_cache_disk` is the path you specified in your vHost file for cache

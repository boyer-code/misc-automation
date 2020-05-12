# misc-automation
repository for my non-network OS specific automation worth sharing


## pihole-tasks-playbook Functions


### Playbook --tags

#### Gravity
- --gravity
  - This command is crucial to Pi-hole as it downloads and processes ad block lists from several sources and combining them into a single gravity.list hosts file, which is used to block ads.
> Note: By default, this command runs once a week via cron, so there’s no need to run it manually unless you want to get some updated lists or you run into a problem with the list.

#### Restart DNS

- --restart_dns
> Note: This will force a reload of dnsmasq at which time it will also reload the config file and the hosts file.

#### Logging


-  --disable_logs|enable_logs

   - Disable/Enable the Pi-hole log at `/var/log/pihole.log`. This can be useful if you don’t want queries logged for a certain time.
- --flush_logs

   - Flushing The Log File
Depending on your system and how heavily your Pi-hole is used, you may want to flush the log throughout the day. By default, the log if flushed at the end of the day via cron, but a very large log file can slow down the Web interface, so flushing it can be useful.
     > NOTE: if you flush the log, some of the stats will not be processed by FTL and thus may not show up in long-term stats.

##### Credits

https://discourse.pi-hole.net/t/the-pihole-command-with-examples/738

##### validated in pihole v5

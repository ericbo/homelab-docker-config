# Docker VM Configs
This is a repo I quickly setup to prevent me from losing any of my docker-compose files.

## Present Homelab Setup
My homelab currently consists of a Dell R710 running XCP-ng with a docker VM running the majority of my services.
All storage is handled by a seconday server running FreeNAS with two pools. The first pool is for non-critical data (48TB raw/32TB usable)
and the second pool for crytical data (12TB raw/6TB usable). Both pools are running raid6-z2 with 6 and 4 drives respectively.
The R710 has a direct ethrnet connection to the FreeNAS server for all iSCSI/SMB traffic for security/performance reasons. 

## Future Setup
In the next 2-3 years I plan on upgrading from a single R710 to two more modern machines. These will both run XCP-ng
allowing me to run a docker VMs on each. Coupled with kubernetes, the goal is to have failover for all my docker services.
This is useful for when a docker VM or XCP-ng server need to restart for updates to take effect.

## Todo
The goal of my homelab is to essentially "download the internet," or at least the parts of it I use the most.
Growing up with Dialup and DSL from a company that specialized in offering spotty service, I've always wanted
to reduce my need to be constantly connected to the internet. This coupled with the fact that I want to eventually
move to an rural area has pushed me to download the resources I use the most. Being a software developer and
doing system administration as a hobby, the majority of my services will be mirrors for code/distro/documentation
repositories.

- [ ] Wikipedia mirror
- [✓] apt-mirror for Debian based distros
- [ ] Python pip mirror
- [ ] PHP Packagist mirror
- [ ] Java Maven mirror
- [ ] C++ conan mirror (never used conan for public libs, so this will be fun)
- [ ] Steam/Battle.net/Uplay/Origin mirrors

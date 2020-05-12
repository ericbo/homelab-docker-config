# Usernet Docker Compose
This application stack is still a work in progress. There is nothing more fustration for me than to have
to remeber passwords and ports. For this reason I plan on having most of my docker service sit behind
a nginx proxy that will handle client-side certificate authentication. The proxy also allows me to
route a given domain name to specific ports in my stack, removing the need to memorize them.

To prevent me from having to have a "master" proxy routing to each docker-compose proxy,
I have opted to use macvlan's for each of my docker stacks. This allows me to assign
each docker-compose file an IP address which can then be mapped to my DNS server.

# Todo
- Add client-side certificate authentication.
- Enabled DNS for macvlans (I prefer to assign static IPs from my router, preventing IP conflics due to human error).

# Sources
- http://tonylawrence.com/posts/unix/synology/free-your-synology-ports/
- https://fardog.io/blog/2017/12/30/client-side-certificate-authentication-with-nginx/
- https://collabnix.com/2-minutes-to-docker-macvlan-networking-a-beginners-guide/
- https://docs.docker.com/compose/compose-file/compose-file-v2/#ipv4_address-ipv6_address
- https://docs.docker.com/compose/networking/#use-a-pre-existing-network

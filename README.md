# Block-Facebook-on-IPtables-Firewall

## details of how to use this script
1. first of all you need to install iptables:
    - sudo apt-get install iptables # on ubuntu
2. then check terminal if it works correctly:
    - man iptables
3. to check firewall policy apply this:
    - sudo iptables -L # by default filter option applyied
4. Some employers like to block access to Facebook to their employees
    - when we apply this: sudo iptables -A OUTPUT -p tcp -d $ip_address_mask -j DROP
    - facebook can't be accessed from your browser
5. to delete the firewall rule apply this one:
    - sudo iptables -D OUTPUT -1 


## resource
* [Linux Iptables Firewall Simplified Examples!](https://likegeeks.com/linux-iptables-firewall-examples/)
* [A Tutorial for Controlling Network Traffic with iptables!](https://www.linode.com/docs/security/firewalls/control-network-traffic-with-iptables/)
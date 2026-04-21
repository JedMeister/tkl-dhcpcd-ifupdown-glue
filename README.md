tkl-dhcpcd-ifupdown-glue
========================

Provides ifupdown glue hook scripts to keep `dhcpcd.conf` and
`/etc/network/interfaces` in sync.

If an interface is configured as either 'static' or 'manual', `ifup`
dynamically adds config to `/etc/dhcpcd.conf` to disable DHCP for that
interface.

When an interface is bought down, config is removed from `/etc/dhcpcd.conf` to
ensure that manually invoking `dhcpcd` still works as expected.

Supports enabling/disabling IPv4 and IPv6 DHCP separately via interfaces file.

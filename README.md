# Bitcoin ABC

- Creates virtual server(s) with docker
- Creates cloud volume(s) and mount to /srv
- Register server(s) in domain `var.domain`
- Creates cloud firewall and apply network policy to server(s)
- Deploy bitcoin-abc in `/srv/bitcoin`

## Components

_Bitcoin ABC_ is a full node implementation of the Bitcoin Cash protocol.

- Original software git repo: <https://github.com/Bitcoin-ABC/bitcoin-abc.git>
- Docker image git repo: <https://github.com/4ops/docker-bitcoin-abc.git>

## Cloud resources

- DigitalOcean droplet
- DigitalOcean volume
- DigitalOcean cloud firewall

## Default firewall rules

### Incoming

- Allow SSH from `var.trusted_sources`

### Outgoing

- Allow tcp to world
- Allow udp to world
- Allow icmp to world

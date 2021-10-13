# pihole-dnscrypt-proxy
A docker compose template that allows running [pi-hole](https://github.com/pi-hole/pi-hole) and [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy).

client -> pi-hole -> dnscrypt-proxy -> dns-servers

# Requirements

- docker-compose (file format > 3.4)
- available port 53

# Setup

- choose password
- customize http port

# Run

`docker-compose up -d`

access admin dashboard at http://host:port/admin

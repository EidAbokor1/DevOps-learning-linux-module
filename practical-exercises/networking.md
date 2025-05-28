# Networking Basics

## Checking Network Interfaces
- `ifconfig` or `ip addr` — Show network interface info and IP addresses

## Testing Connectivity
- `ping google.com` — Test connectivity to a host

## SSH Access
- `ssh -i key.pem user@public-ip` — Connect to remote server using private key

> **Note:** SSH requires a public IP or access via VPN / bastion host if using private IPs.

# NAT vs Bridged vs Host Only:

| Connection Type | VM <--> Host | VM1 <--> VM2 | VM -> Internet | VM <- Internet (Port Forwarding) |
|-----------------|------------|------------|----------------|----------------------------------|
| Host-only       | +          | +          | -              | -                                |
| Internal        | -          | +          | -              | -                                |
| Bridged         | +          | +          | +              | +                                |
| NAT             | -          | -          | +              | Port forwarding                  |
| NAT Network     | -          | +          | +              | Port forwarding                  |






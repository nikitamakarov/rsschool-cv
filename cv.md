# Nikita Makarov

This is a test CV for the RS School course which does not reflect the actual CV. Sorry about that.

## Contacts

On demand

## Brief

Some experience with backend and infrastructure. Learning frontend to enter the brave new world of full-stack development.

## Skills

IT infrastructure, cloud, devops, backend

## Code samples

```shell
router bgp 64512
 template peer-policy AS64512
  route-map AS64512-in in
  route-map AS64512-out out
  advertisement-interval 1
  soft-reconfiguration inbound
  send-community
  allowas-in 1
 exit-peer-policy
 !
 template peer-session AS64512
  remote-as 64512
  transport path-mtu-discovery
  description Demo
  password 7 [removed]
  ebgp-multihop 3
  timers 3 9
 exit-peer-session
 !
 bgp router-id 192.0.2.0
 bgp log-neighbor-changes
 !
 address-family ipv4 vrf Demo
  redistribute static
  neighbor 192.0.2.1 activate
  neighbor 192.0.2.1 inherit peer-policy AS64512
  neighbor 192.0.2.1 inherit peer-session AS64512
  neighbor 192.0.2.1 description Demo
  no auto-summary
  no synchronization
 exit-address-family
```

## Work experience

On demand.


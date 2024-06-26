# config
underlay - control-plane - unicast: ospf
underlay - control-plane - bum: ir w/ ibgp
overlay - control-plane: evpn w/ ibgp
overlay - data-plane: evpn w/ vxlan

## ref.
Chap. 5: Single AS Model with OSPF Underlay
VXLAN Fabric with BGP EVPN Control-Plane: Design Considerations

# show
## preparation
show ip interface brief

## underlay
show cli history unformatted
show ip ospf neighbors 
show ip pim rp
show ip pim neighbor 
show run bgp
show bgp l2vpn evpn summary

## overlay l2 bridging
ping 192.168.10.12 count unlimited interval 1
show run vlan
show run interface nve 1
show bgp l2vpn evpn summary
show bgp l2vpn evpn
show run | sec evpn
show vxlan
show nve interface 
show nve vni
show mac address-table dynamic

This simple network project is based off of the one I saw on this website: https://gurutechnetworks.otombenard.com/assetsProject/project1

Simple Network Topology - CCNA Project
Description
This project demonstrates a Simple Network Topology built using Cisco Packet Tracer for the purpose of CCNA exam preparation. The network is divided into two departments: Accounts and Delivery, each with its own subnet, routers, switches, and end devices (PCs). The routers are configured to allow inter-departmental communication between the two subnets using OSPF (Open Shortest Path First), a dynamic routing protocol.

Network Layout
Accounts Department (192.168.40.0/29):
    5 PCs (Accounts PC1 to PC5).
    Connected to Accounts Switch (2960-24TT).
    Accounts Router (2911) configured with OSPF and connected to the switch and the Delivery Router.

Delivery Department (192.168.41.8/29):
    5 PCs (Delivery PC1 to PC5).
    Connected to Delivery Switch (2960-24TT).
    Delivery Router (2911) configured with OSPF and connected to the switch and the Accounts Router.

Network Components
    Routers:
        Accounts Router (2911): Manages routing for the Accounts department, configured with OSPF.
        Delivery Router (2911): Manages routing for the Delivery department, configured with OSPF.

Both routers are interconnected via a serial link and share OSPF routing information to enable communication between the two departments.
    Switches:
        Accounts Switch (2960-24TT): Connects PCs in the Accounts department.
        Delivery Switch (2960-24TT): Connects PCs in the Delivery department.
    PCs:
        Accounts PCs (192.168.40.x): Devices in the Accounts department.
        Delivery PCs (192.168.41.x): Devices in the Delivery department.
    Subnets
        Accounts Department: 192.168.40.0/28 (14 usable IPs).
        Delivery Department: 192.168.41.8/29 (6 usable IPs).

Both routers participate in OSPF Area 0 (the backbone area) to exchange route information, enabling efficient communication between the two subnets.
OSPF ensures that the routers dynamically learn routes to each other's subnets without the need for static routes, making the network more scalable and flexible.

My Objectives

Implement a simple network with two distinct subnets for two departments.
Enable dynamic routing using OSPF for inter-departmental communication.
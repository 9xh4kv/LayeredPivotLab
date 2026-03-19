> **Read the full write-up at [Pivoting with Ligolo-ng](https://9xh4kv.dev/blog/posts/2026/0319-ligolo-ng.html)**  
> Step-by-step guide covering pivoting, relays, and routing with Ligolo-ng.

# LayeredPivotLab
A small Docker-based lab that simulates a realistic, segmented enterprise network for practicing pivoting and lateral movement techniques.

## Purpose
Designed for hands-on exercises including single pivot, double pivot, multi-hop tunneling, routing, listener setup, and general lateral movement in segmented networks.

## Network layout
The lab consists of four hosts connected across three segmented networks:

> **Note:** All hosts use the same credentials for simplicity `root` : `password`

**attacker-pc**

IP address: `10.10.0.20`

Located on the external network (`10.10.0.0/24`) and used as the attacking machine.

**external-host**

IP addresses: `10.10.0.2`, `192.168.10.2`

Public-facing server that bridges the external network to the internal network.

**internal-pc**

IP addresses: `192.168.10.3`, `172.25.1.3`

Internal workstation that provides access to a deeper isolated segment.

**isolated-db**

IP address: `172.25.1.4`

Backend database server residing within the isolated network (`172.25.1.0/24`).

![NetworkLayout](https://9xh4kv.github.io/blog/assets/images/20260319-ligolo-ng2.png?raw=true)

## Ligolo-ng Ready

The `agent` and `proxy` binaries are pre-placed in `/root/` on the **attacker-pc** container.

> **Read the full write-up at [Pivoting with Ligolo-ng](https://9xh4kv.dev/blog/posts/2026/0319-ligolo-ng.html)**  
> Step-by-step guide covering pivoting, relays, and routing with Ligolo-ng.

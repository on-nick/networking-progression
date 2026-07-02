# Day 05 – Subnetting Mastery

## 🎯 Objective

The objective of Day 05 was to develop a strong understanding of IPv4 subnetting. I focused on calculating network and broadcast addresses, determining valid host ranges, calculating the number of usable hosts in different subnet sizes, identifying whether two IP addresses belong to the same subnet, and designing IP addressing schemes for small networks.

---

# 📚 Concepts Learned

## 1. Network Address

The network address is the first IP address in a subnet. It uniquely identifies the network and cannot be assigned to any host.

Example:

* IP Address: `192.168.10.35/27`
* Network Address: `192.168.10.32`

---

## 2. Broadcast Address

The broadcast address is the last IP address in a subnet. It is used to send packets to every device within that subnet.

Example:

* Broadcast Address: `192.168.10.63`

---

## 3. Valid Host Range

The usable host addresses lie between the network and broadcast addresses.

Example:

Network: `192.168.10.32`

Broadcast: `192.168.10.63`

Usable Hosts:

```
192.168.10.33
to
192.168.10.62
```

---

## 4. Number of Hosts

Formula:

```
Usable Hosts = 2^(Host Bits) - 2
```

Examples:

| Prefix | Host Bits | Usable Hosts |
| ------ | --------: | -----------: |
| /24    |         8 |          254 |
| /25    |         7 |          126 |
| /26    |         6 |           62 |
| /27    |         5 |           30 |
| /28    |         4 |           14 |
| /29    |         3 |            6 |
| /30    |         2 |            2 |

---

## 5. Identifying Whether Two IPs Are in the Same Subnet

Steps:

1. Find the subnet mask.
2. Calculate the network address of both IP addresses.
3. Compare the network addresses.
4. If they match, both IPs belong to the same subnet.

---

## 6. Small Company IP Address Design

Example:

Company requires four departments:

| Department | Required Hosts | Assigned Subnet  |
| ---------- | -------------: | ---------------- |
| HR         |             25 | 192.168.1.0/27   |
| Finance    |             20 | 192.168.1.32/27  |
| IT         |             50 | 192.168.1.64/26  |
| Management |             10 | 192.168.1.128/28 |

This exercise demonstrated how subnetting efficiently utilizes available IP addresses.

---

#  Subnetting Exercises

### Exercise 1

Given:

```
IP: 192.168.10.45/27
```

Answer:

* Network Address: `192.168.10.32`
* Broadcast Address: `192.168.10.63`
* Valid Hosts:

  * `192.168.10.33`
  * `192.168.10.62`
* Total Usable Hosts: **30**

---

### Exercise 2

Given:

```
IP: 10.0.5.130/25
```

Answer:

* Network Address: `10.0.5.128`
* Broadcast Address: `10.0.5.255`
* Valid Hosts:

  * `10.0.5.129`
  * `10.0.5.254`
* Total Usable Hosts: **126**

---

### Exercise 3

Determine whether these IP addresses belong to the same subnet.

```
192.168.1.10/24
192.168.1.200/24
```

Result:

✅ Yes

Both belong to network:

```
192.168.1.0/24
```

---

### Exercise 4

Determine whether these IP addresses belong to the same subnet.

```
192.168.1.10/26
192.168.1.100/26
```

Result:

❌ No

Networks:

```
192.168.1.0/26
192.168.1.64/26
```

---

#  Packet Tracer Lab

### Lab Objective

Create a simple network consisting of:

* 1 Router
* 2 Switches
* 4 PCs

Tasks performed:

* Connected all devices correctly.
* Assigned IP addresses according to subnet boundaries.
* Configured subnet masks.
* Set default gateways.
* Verified connectivity using `ping`.
* Confirmed that hosts within the same subnet communicated successfully.

---

# Problems Encountered

* Initially confused the network address with the first usable host address.
* Occasionally miscalculated block sizes for different subnet masks.
* Needed additional practice determining subnet boundaries without using online calculators.
* Accidentally assigned a broadcast address to a host during one practice exercise.

---

# How I Solved Them

* Practiced subnetting problems repeatedly until calculations became faster.
* Used binary conversion to verify subnet boundaries.
* Memorized common subnet masks and their corresponding block sizes.
* Verified every answer manually before checking with a subnet calculator.
* Built Packet Tracer labs to reinforce the concepts with practical implementation.


---

##  Day 05 Summary

Today's learning significantly improved my understanding of IPv4 subnetting. I can now calculate network and broadcast addresses, determine valid host ranges, identify whether two devices belong to the same subnet, estimate the number of usable hosts, and design efficient IP addressing schemes for small networks. Through both theoretical exercises and Packet Tracer practice, I strengthened my confidence in applying subnetting concepts to real-world networking scenarios.

**Status:** ✅ Completed Day 05 – Subnetting Mastery

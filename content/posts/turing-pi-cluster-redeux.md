+++
categories = [
    "cloud",
    "tech"
]
date = 2024-05-12T19:20:56Z
draft = false
tags = [
    "turing-pi-2",
    "distributed",
    "rPi",
    "Jetson"
]
title = "Turing Pi Cluster - Part the Second"
+++

# Update

## Case.
![](/KXRORS-S450.webp)
I have installed the first host board in a [KXRORS S450](https://www.amazon.com/KXRORS-S450-Water-Cooling-Motherboard-Case-Black/dp/B0CQNW7XXK)
case.  It is a nice case but it has a few issues I need to work out.  The other plan is a custom acrylic case.

## Storage 
![](/samsung-pro-2TB.webp)
The TuringPi 2 has 4 NVMe slots (one for each compute board).  The slots are PCIe gen3 but it is just as cheap (or cheaper)
to buy gen4 boards.  I populated the host with [Samsung 990 Pros 2TB](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/990-pro-pcie-4-0-nvme-ssd-2tb-mz-v9p2t0b-am/)

## Provisioning
I am practicing my Ansible with these nodes and will be provisioning solely via this means.

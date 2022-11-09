+++
categories = ["tech"]
date = 2022-10-25T23:37:32Z
draft = false
tags = [
  "proxmox",
  "virtual machines",
  "administration",
]
title = "Creating Vm Template in Proxmox"
+++
 - * Download image from https://cloud-images.ubuntu.com/minimal/releases/jammy/release/ubuntu-22.04-minimal-cloudimg-amd64.img
 - * attach VGA console `qm set $VM_ID --serial0 socker --vga serial0`
 - * rename the image to `qcow2`  e.g., `mv ubuntu-22.04-minimal-cloudimg-amd64.img ubuntu-22.04-cloud.qcow2`
 - * resize the image `qemu-img resize ubuntu-22.04-cloud.qcow2 30G`
 - * import image into proxmox `qm importdisk $VM_ID ubuntu-22.04-cloud.qcow2 local-lvm`

Heavy Inspiration drawn from this [blog/video](https://www.learnlinux.tv/proxmox-ve-how-to-build-an-ubuntu-22-04-template-updated-method/)

+++
categories = ["tech"]
date = 2023-08-17T01:53:45Z
tags = [
  "home network",
  "10g"
]
title = "Bus Speed"
+++
# Speeds of various transports
> Convention:  
>* Lowercase B always means a bit 
>* Uppercase B always means a byte 
>* Byte is defined as 8 bits.

## Disk Drives
tbd

## Ethernet
tbd

## PCIe
| Version     | Transfer Rate (per lane) | x1 | x4 | x8 | x16 | 
| -------- | ------- | -------- | ------- | -------- | ------- |
| 1.0  | 2.5 GT/s | 0.25 GB/s | 1 GB/s | 2 GB/s | 4 GB/s |
| 2.0  | 5 GT/s | 0.5 GB/s | 1GB/s | 4GB/s | 8 GB/s |
| 3.0  | 8 GT/s | 0.985 GB/s | 3.938 GB/s | 7.877 GB/s | 15.754 GB/s |
| 4.0  | 16 GT/s | 1.969 GB/s | 7.877 GB/s | 15.754 GB/s| 31.508 GB/s |
| 5.0  | 32 GT/s | 3.938 GB/s | 15.754 GB/s| 31.508 GB/s | 63.015 GB/s |
| 6.0  | 64 GT/s | 7.563G B/s | 31.508 GB/s | 63.015 GB/s | 121 GB/s |
| 7.0*  | 128 GT/s | 15.125GB/s | 63.015 GB/s | 121 GB/s | 242 GB/s

\* Stilling being worked on as of2023/08/17
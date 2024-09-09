---
title: Dummy post
date: 2020-05-25 23:22:33
categories: [Back-end]
tags: [AWS, DevOps]
---

# This is a dummy post

{% asset_img "spider_files.jpg" "A self-portrait, hanging upside down while throwing spider webs to files" %}

## Text

This a dummy file, with category, tags, an image and and a mermaid graph.

This is some **bold text**, some *italics text* and come **_bold plus italics text_**.

---

## Code

```java
System.out.println("Hello world");
```

## Graphic

This is a mermaid graph.

```mermaid
graph TD

A(Internet)
B[Cable/Modem]
C[Router/Switch]
D[Firewall]
E[Device 1]
F[Device 2]

G(Internet)
H[Internet Gateway]
I[Route Table]
J[Network Access Control List - NACL]
K[EC2 instance 1]
L[EC2 instance 2]

subgraph Home
  A-->B
  B-->C
  C-->D
  D-->E
  D-->F
end

subgraph VPV
  G-->H
  H-->I
  I-->J
  J-->K
  J-->L
end
```

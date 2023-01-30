# A Deep Dive into Hashing and Cryptographic hashes!

## Introduction to hashing:

Let's start things with hashing, hash function is a function which takes an input of any size and turns it into a fixed-size output. hashing is like it will take value from you and spit out a hashed function which is not readable at all, it is used mainly for privacy reasons. These inputs get larger from top to bottom but always map to an output of 32 bytes. now let's talk about **CRYPTOGRAPHIC HASH!**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675065175351/253614d1-dd0d-4f4d-beb6-8e18ca128b59.jpeg align="center")

## Cryptographic hash:

A cryptographic hash is used to create a secure, fixed-size representation even though the input can be anything.. text, a photo or a video. This is very useful in decentralisation as privacy is the main point of it. In many cases, the blockchain will not store the input and directly store the hashed output. Hashing can be performed in code using a tool known as sha256 and it is available here: [https://emn178.github.io/online-tools/sha256](https://emn178.github.io/online-tools/sha256)

## What is sha256?

**sha256** helps us to get a 256 bits-hashed output. But there are still security concerns, some of the primary features of the crypto hash are

1\. Deterministic

2\. One-way

3\. Pseudorandom

4\. Fast to compute

5\. Collison Resistant

## Is it always that secure?

It is really the one-way part which makes hashing so secure, it is difficult to guess the input with the help of the output as the combinations can be as high as 2^256 and vice versa. It is impossible though. Hackers can guess your input by brute force by comparing your hash with other input hashes, in this way, they can get an idea of what your information might be, known as a rainbow bridge, but it is still quite tricky.

that's for today folks. see you soon. keep building!

[  
](https://twitter.com/subhamstwt/status/1615813257465565184)[  
](https://twitter.com/subhamstwt/status/1615813251601948672)

[  
](https://twitter.com/subhamstwt/status/1615813238268231680)

[  
](https://twitter.com/subhamstwt/status/1615813233855827969)
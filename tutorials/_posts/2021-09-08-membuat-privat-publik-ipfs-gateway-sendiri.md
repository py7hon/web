---
layout: post
title:  "Membuat Privat/Publik IPFS Gateway Sendiri"
date:   2021-09-08 20:45:00 +0200
category: tutorials
---

# Membuat Privat/Publik IPFS Gateway Sendiri
![webui](https://files.catbox.moe/grxd4x.png)

**IPFS** adalah Sistem File InterPlanet adalah protokol dan jaringan peer-to-peer untuk menyimpan dan berbagi data dalam sistem file terdistribusi. IPFS menggunakan pengalamatan konten untuk secara unik mengidentifikasi setiap file dalam namespace global yang menghubungkan semua perangkat komputasi.

Kali ini saya menggunakan OS Debian.

## Download Dist File IPFS
```terminal
# wget https://dist.ipfs.io/go-ipfs/v0.9.1/go-ipfs_v0.9.1_linux-amd64.tar.gz
```
## Ekstrak File dan Install
```terminal
# tar xvfz go-ipfs_v0.9.1_linux-amd64.tar.gz
go-ipfs/install.s
go-ipfs/ipfs
go-ipfs/LICENSE
go-ipfs/LICENSE-APACHE
go-ipfs/LICENSE-MIT
go-ipfs/README.md
```
```terminal
# cd go-ipfs
```
```terminal
# ./install.sh
Moved ./ipfs to /usr/local/bin
```
## Tes IPFS versi
```terminal
# ipfs --version
ipfs version 0.9.1
```
## Initialize IPFS
```terminal
# IPFS_PATH=~/.ipfs ipfs init --profile server
generating ED25519 keypair...done
peer identity: 12D3KooWKQn2n8Yee75qJqUHAc6cpfZypby2qhczWhXYx2k4FEtM
initializing IPFS node at /root/.ipfs
to get started, enter:

        ipfs cat /ipfs/QmQPeNsJPyVWPFDVHb77w8G42Fvo15z4bG2X8D2GhfbSXc/readme
```
```terminal
# ipfs cat /ipfs/QmQPeNsJPyVWPFDVHb77w8G42Fvo15z4bG2X8D2GhfbSXc/readme
```
![ipfs](https://files.catbox.moe/ov0pl2.png)

## Membuat Systemd Service untuk IPFS
```terminal
# nano /etc/systemd/system/ipfs.service
```
dan paste script di bawah ini
```service
[Unit]
Description=IPFS Daemon
After=syslog.target network.target remote-fs.target nss-lookup.target

[Service]
Type=simple
ExecStart=/usr/local/bin/ipfs daemon --enable-namesys-pubsub
User=root
[Install]
WantedBy=multi-user.target
```
untuk mengaktifkan service nya
```terminal
# systemctl enable ipfs
```
dan untuk memulai nya
```terminal
# systemctl start ipfs
```
dan untuk mengecek status dari service nya berjalan atau tidak
```terminal
# systemctl status ipfs
● ipfs.service - ipfs daemon
   Loaded: loaded (/lib/systemd/system/ipfs.service; enabled; vendor preset: enabled)
   Active: active (running) since Wed 2021-09-05 20:38:04 UTC; 4s ago
 Main PID: 30133 (ipfs)
    Tasks: 9 (limit: 4915)
   CGroup: /system.slice/ipfs.service
           └─30133 /usr/local/bin/ipfs daemon --enable-gc

ipfs[30133]: Swarm listening on /ip4/127.0.0.1/tcp/4001
ipfs[30133]: Swarm listening on /ip4/172.31.43.10/tcp/4001
ipfs[30133]: Swarm listening on /ip6/::1/tcp/4001
ipfs[30133]: Swarm listening on /p2p-circuit
ipfs[30133]: Swarm announcing /ip4/127.0.0.1/tcp/4001
ipfs[30133]: Swarm announcing /ip6/::1/tcp/4001
ipfs[30133]: API server listening on /ip4/127.0.0.1/tcp/5001
ipfs[30133]: WebUI: http://127.0.0.1:5001/webui
ipfs[30133]: Gateway (readonly) server listening on /ip4/127.0.0.1/tcp/80
ipfs[30133]: Daemon is ready
```

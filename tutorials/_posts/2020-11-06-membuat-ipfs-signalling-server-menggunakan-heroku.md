---
layout: post
title:  "Membuat IPFS Signalling Server Menggunakan Heroku"
date:   2021-11-06 16:45:00 +0200
category: tutorials
---

# ![1636195625](https://user-images.githubusercontent.com/29944979/140606665-1420a897-dd7f-468d-bd47-a0bed99fab22.png)

Sebelum nya kita berkenalan dengan Signaling-Server terlebih dahulu.

**Signaling-Server** adalah atau digunakan di **libp2p** untuk mengizinkan browser dan klien dengan penerusan port terbatas
untuk berkomunikasi dengan rekan-rekan lain di jaringan **libp2p**.

Dan sebelum nya saya membuat **[Uup](https://uup.bugs.today)** dan mendapatkan error 
`Error: no valid addresses were provided for transports [WebSockets,WebRTCStar,Circuit]` pada `js-ipfs`.

Lalu saya mencaritahu nya pada halaman Issue di repository `js-ipfs` dan saya menemukan tautan yang mengarahkan kepada twit

> [@ThePatToner](https://twitter.com/ThePatToner?ref_src=twsrc%5Etfw)  
> I see that you are trying to listen on a websocket-star address.
> Unfortunately, we did a poor job on announcing it, but we are no
> supporting websocket-star addresses since js-ipfs@0.41
> 
> — Vasco Santos (@vascosantos10) [May 19,
> 2020](https://twitter.com/vascosantos10/status/1262769647482482689?ref_src=twsrc%5Etfw)

yang mana pada versi `js-ipfs@0.41` sudah tidak di dukung lagi untuk memakai `websocket`.
Dan karena itu saya mencoba membuat sendiri **Signaling-Server** dengan **Heroku**.

### 1. Login akun Heroku pada Heroku-CLI
```bash
$ heroku login
```
### 2. Login Container Registry
```bash
$ heroku container:login
```
### 3. Clone repository webrtc-star
```bash
$ git clone https://github.com/libp2p/js-libp2p-webrtc-star.git
$ cd js-libp2p-webrtc-star
```
### 4. Membuat Heroku app
```bash
$ heroku create
```
### 5. Build dan push the image
```bash
$ heroku container:push web
```
### Rilis image ke app yang telah dibuat
```bash
$ heroku container:release web
```
### Skalakan ke satu worker gratis
```bash
$ heroku ps:scale web=1
```
###  Buka app dalam browser
```bash
$ heroku open
```
Dan selesai sudah Tutorial Membuat IPFS Signalling Server Menggunakan Heroku.

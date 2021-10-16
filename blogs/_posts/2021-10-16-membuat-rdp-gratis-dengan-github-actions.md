---
layout: post
title:  "Membuat RDP Gratis dengan Github Actions"
date:   2021-10-16 22:30:00 +0200
updated: 2021-10-17 00:24:00 +0200
category: blogs
---

# Membuat RDP Gratis dengan Github Actions

###### ⚠️ USE AT YOUR OWN RISK ⚠️

Hallo, Saya ingin membagikan tutorial mendapatkan RDP gratis* dengan menggunakan RemoteDesktop dari chrome dan Github Actions.

## 1. Membuat sebuah repository pada Github

Kamu harus membuat repository dahulu pada Github, di utamakan yang kosong dan tidak ada file/folder.

## 2. Buatlah sebuah file

Untuk tahap ini kalian bisa menggunakan kode editor apapun yang kalian suka, lalu kalian buat file yang bernama `setup.ps1` dan `timeout.ps1`.
Berikut adalah contoh kode nya.

- `setup.ps1`

```powershell
Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False
& {$P = $env:TEMP + '\chromeremotedesktophost.msi'; Invoke-WebRequest 'https://dl.google.com/edgedl/chrome-remote-desktop/chromeremotedesktophost.msi' -OutFile $P; Start-Process $P -Wait; Remove-Item $P}
& {$P = $env:TEMP + '\chrome_installer.exe'; Invoke-WebRequest 'https://dl.google.com/chrome/install/latest/chrome_installer.exe' -OutFile $P; Start-Process -FilePath $P -Args '/install' -Verb RunAs -Wait; Remove-Item $P}
```

- `timeout.ps1`

```powershell
$i = 360
do {
    Write-Host $i
    Sleep 60
    $i--
} while ($i -gt 0)
```

## 3. Push ke Github

Jika kalian sudah menjalankan tahap nomor **2** kalian bisa push file tersebut ke repository yang kalian buat tadi pada tahap **1**.

## 4. Buka Action pada Repository 

Kalau kalian sudah Push file ke repository kalian bisa buka page Actions dan salin kode dibawah ini.

```yaml
name: Windows-CRD

on: 
  workflow_dispatch:
    inputs:
      authcode:
        description: 'Enter CRD code'
        required: true
      pincode:
        description: 'Eight digit Pin'
        required: true
  
jobs:
  build:
    runs-on: windows-latest

    steps:
    - uses: actions/checkout@v2
    - name: Initializing Setup
      run: ./setup.ps1
    - name: Starting CRD
      run: ${{ github.event.inputs.authcode }} -pin=${{ github.event.inputs.pincode }}
    - name: Keep Alive
      run: ./timeout.ps1
```

## 5. Buka Website Remote Desktop dan Setup

Jika kalian sudah melakukan tahap **4** lalu buka website RemoteDesktop pada link di bawah dengan akun Google kamu

[https://remotedesktop.google.com/headless](https://remotedesktop.google.com/headless)

dan salin kode pada **Windows (PowerShell)** seperti di gambar bawah ini

![COPY](https://files.catbox.moe/gr91fs.jpg)

dan paste pada **Run workflow** seperti gambar di bawah ini

![CDR](https://files.catbox.moe/pce82t.jpg)

dan kamu berikan pin seperti gambar dibawah ini dan klik run workflow

![PIN](https://files.catbox.moe/npyley.jpg)

## 6. Akses RDP
Jika kamu sudah menjalankan workflow kamu tinggal membuka Website Remote Desktop untuk mengakses RDP nya.

#### Note
- PIN
Jika kamu mendapakan masalah seperti di gambar bawah ini kamu harus memasukan PIN yang sudah di buat pada tahap **5**.

![PIN](https://files.catbox.moe/coi4q2.jpg)

- Speed RDP

![SPEED](https://files.catbox.moe/k5ppnt.jpg)

###### * Ingat saya tidak menganjurkan anda untuk menyalahgunakan nya, saya membuat ini hanya untuk kepentingan penelitian dan pembelajaran.

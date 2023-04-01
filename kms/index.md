---
layout: page
title: KMS
updated: 2022-10-17 11:41:00 +0200
---
## KMS Windows
<hr style="width:40%">
Aktivator KMS semua versi Windows, semua versi office, dan aktifkan Windows dengan satu perintah dengan gratis.
<br/>

## Cara Penggunaan:

### 1. Activate Windows

Jika Windows Anda adalah versi VL, maka jalankan saja dua perintah berikut di cmd atau PowerShell dengan hak administrator.

Setelah menjalankan perintah pertama, tunggu jendela prompt muncul, di mana komputer harus terhubung ke Internet.

<pre>
slmgr /skms kms.iqbalrifai.eu.org

slmgr /ato
</pre>

Jika ini bukan versi VL, Anda perlu mengubah kunci untuk mendapatkan KUNCI versi yang sesuai, sebagai berikut:

Jalankan perintah berikut untuk melihat versi sistem:

<pre>
wmic os get caption
</pre>

Temukan kunci yang sesuai di akhir artikel, dan jalankan perintah berikut untuk menginstal kunci di cmd atau PowerShell dengan hak administrator:

<pre>
slmgr /ipk xxxxx-xxxxx-xxxxx-xxxxx
</pre>

Kemudian atur alamat server KMS seperti yang disebutkan di atas dan aktifkan.

**Misalnya: cara mengaktifkan setelah menginstal Windows 10 Enterprise Edition yang baru**

Jika Anda baru atau sudah menginstal Windows 10 Enterprise Edition, maka Anda hanya perlu menyalin perintah berikut untuk menjalankannya di cmd atau powershell dengan hak administrator langsung.

<pre>
slmgr.vbs /upk

slmgr /ipk NPPR9-FWDCX-D2C8J-H872K-2YT43

slmgr /skms kms.iqbalrifai.eu.org

slmgr /ato
</pre>

### 2. Activate Office

Jalankan perintah berikut di cmd atau PowerShell dengan hak administrator untuk masuk ke direktori penginstalan Office 2016 32-bit atau 64-bit.

(Tergantung pada apakah Anda menginstal Office 32-bit atau 64-bit ke salah satu direktori ini):

<pre>
32-bit jalankan perintah berikut:

cd "C:\Program Files (x86)\Microsoft Office\Office16"

64-bit jalankan perintah berikut:

cd "C:\Program Files\Microsoft Office\Office16
</pre>

Jalankan dua perintah berikut di cmd atau PowerShell dengan hak administrator. 
Setelah menjalankan perintah pertama, tunggu baris perintah muncul untuk umpan balik, di mana komputer harus terhubung ke Internet.

<pre>
cscript ospp.vbs /sethst:kms.iqbalrifai.eu.org

cscript ospp.vbs /act
</pre>

Jika Anda melihat kata berhasil saat diminta, maka aktivasi berhasil, buka kembali Office.

### 3. 1 Klik Install

Kamu hanya perlu membuka PowerShell lalu menjalankan perintah di bawah ini:

<pre>
irm https://s.id/get-kms | iex
</pre>

Lalu ikuti langkah nya yang tertera pada PowerShell.

<hr style="width:40%">

<h5 class="ml-3 mt-3">Windows Server 2022</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows Server 2022 Datacenter</td>
<td>WX4NM-KYWYW-QJJR4-XV3QB-6VM33</td>
</tr>
<tr>
<td>Windows Server 2022 Standard</td>
<td>VDYBN-27WPP-V4HQT-9VMD4-VMK7H</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows Server Version 20H2, 2004, 1909, 1903, 1809</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows Server Datacenter</td>
<td>6NMRW-2C8FM-D24W7-TQWMY-CWH2D</td>
</tr>
<tr>
<td>Windows Server Standard</td>
<td>N2KJX-J94YW-TQVFB-DG9YT-724CC</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows Server Version 1803</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows Server Datacenter</td>
<td>2HXDN-KRXHB-GPYC7-YCKFJ-7FVDG</td>
</tr>
<tr>
<td>Windows Server Standard</td>
<td>PTXN8-JFHJM-4WC78-MPCBR-9W4KR</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows Server Version 1709</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows Server Datacenter</td>
<td>6Y6KB-N82V8-D8CQV-23MJW-BWTG6</td>
</tr>
<tr>
<td>Windows Server Standard</td>
<td>DPCNP-XQFKJ-BJF7R-FRC8D-GF6G4</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows Server 2019</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows Server 2019 Datacenter</td>
<td>WMDGN-G9PQG-XVVXX-R3X43-63DFG</td>
</tr>
<tr>
<td>Windows Server 2019 Standard</td>
<td>N69G4-B89J2-4G8F4-WWYCC-J464C</td>
</tr>
<tr>
<td>Windows Server 2019 Essentials</td>
<td> WVDHN-86M7X-466 P 6-VHXV7-YY726</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows Server 2016</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows Server 2016 Datacenter</td>
<td>CB7KF-BWN84-R7R2Y-793K2-8XDDG</td>
</tr>
<tr>
<td>Windows Server 2016 Standard</td>
<td>WC2BQ-8NRM3-FDDYY-2BFGV-KHKQY</td>
</tr>
<tr>
<td>Windows Server 2016 Essentials</td>
<td>JCKRF-N37P4-C2D82-9YXRT-4M63B</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3" id="win10core">Windows 10 Core</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Win 10 Core</td>
<td>TX9XD-98N7V-6WMQ6-BX7FG-H8Q99</td>
</tr>
<tr>
<td>Win 10 CoreN</td>
<td>3KHY7-WNT83-DGQKR-F7HPR-844BM</td>
</tr>
<tr>
<td>Win 10 CoreSingleLanguage</td>
<td>7HNRX-D7KGG-3K4RQ-4WPJ4-YTDFH</td>
</tr>
<tr>
<td>Win 10 CoreCountrySpecific</td>
<td>PVMJN-6DFY6-9CCP6-7BKTT-D3WVR</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows 10 , Windows 11</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows 10 Professional</br>
Windows 11 Professional
</td>
<td>W269N-WFGWX-YVC9B-4J6C9-T83GX</td>
</tr>
<tr>
<td>Windows 10 Professional N
</br>Windows 11 Professional N</td>
<td>MH37W-N47XK-V7XM9-C7227-GCQG9</td>
</tr>
<tr>
<td>Windows 10 Pro for Workstations
</br>Windows 11 Pro for Workstations</td>
<td>NRG8B-VKK3Q-CXVCJ-9G2XF-6Q84J</td>
</tr>
<tr>
<td>Windows 10 Pro for Workstations N
</br>Windows 11 Pro for Workstations N</td>
<td>9FNHH-K3HBT-3W4TD-6383H-6XYWF</td>
</tr>
<tr>
<td>Windows 10 Pro Education
</br>Windows 11 Pro Education</td>
<td>6TP4R-GNPTD-KYYHQ-7B7DP-J447Y</td>
</tr>
<tr>
<td>Windows 10 Pro Education N
</br>Windows 11 Pro Education N</td>
<td>YVWGF-BXNMC-HTQYQ-CPQ99-66QFC</td>
</tr>
<tr>
<td>Windows 10 Education
</br>Windows 11 Education</td>
<td>NW6C2-QMPVW-D7KKK-3GKT6-VCFB2</td>
</tr>
<tr>
<td>Windows 10 Education N
</br>Windows 11 Education N</td>
<td>2WH4N-8QGBV-H22JP-CT43Q-MDWWJ</td>
</tr>
<tr>
<td>Windows 10 Enterprise
</br>Windows 11 Enterprise</td>
<td>NPPR9-FWDCX-D2C8J-H872K-2YT43</td>
</tr>
<tr>
<td>Windows 10 Enterprise N
</br>Windows 11 Enterprise N</td>
<td>DPH2V-TTNVB-4X9Q3-TJR4H-KHJW4</td>
</tr>
<tr>
<td>Windows 10 Enterprise G
</br>Windows 11 Enterprise G</td>
<td>YYVX9-NTFWV-6MDM3-9PT4T-4M68B</td>
</tr>
<tr>
<td>Windows 10 Enterprise G N
</br>Windows 11 Enterprise G N</td>
<td>44RPN-FTY23-9VTTB-MP9BX-T84FV</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows 10（LTSC/LTSB Version）</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows 10 Enterprise 2015 LTSB</td>
<td>WNMTR-4C88C-JK8YV-HQ7T2-76DF9</td>
</tr>
<tr>
<td>Windows 10 Enterprise 2015 LTSB N</td>
<td>2F77B-TNFGY-69QQF-B8YKP-D69TJ</td>
</tr>
<tr>
<td>Windows 10 Enterprise 2016 LTSB</td>
<td>DCPHK-NFMTC-H88MJ-PFHPY-QJ4BJ</td>
</tr>
<tr>
<td>Windows 10 Enterprise N LTSB 2016</td>
<td>QFFDN-GRT3P-VKWWX-X7T3R-8B639</td>
</tr>
<tr>
<td>Windows 10 Enterprise LTSC 2019</td>
<td>M7XTQ-FN8P6-TTKYV-9D4CC-J462D</td>
</tr>
<tr>
<td>Windows 10 Enterprise N LTSC 2019</td>
<td>92NFX-8DJQP-P6BBQ-THF9C-7CG2H</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows Server 2012 R2 Windows 8.1</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows 8.1 Professional</td>
<td>GCRJD-8NW9H-F2CDX-CCM8D-9D6T9</td>
</tr>
<tr>
<td>Windows 8.1 Professional N</td>
<td>HMCNV-VVBFX-7HMBH-CTY9B-B4FXY</td>
</tr>
<tr>
<td>Windows 8.1 Enterprise</td>
<td>MHF9N-XY6XB-WVXMC-BTDCT-MKKG7</td>
</tr>
<tr>
<td>Windows 8.1 Enterprise N</td>
<td>TT4HM-HN7YT-62K67-RGRQJ-JFFXW</td>
</tr>
<tr>
<td>Windows Server 2012 R2 Server Standard</td>
<td>D2N9P-3P6X9-2R39C-7RTCD-MDVJX</td>
</tr>
<tr>
<td>Windows Server 2012 R2 Datacenter</td>
<td>W3GGN-FT8W3-Y4M27-J84CP-Q3VJ9</td>
</tr>
<tr>
<td>Windows Server 2012 R2 Essentials</td>
<td>KNC87-3J2TX-XB4WP-VCPJV-M4FWM</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows Server 2012 Windows 8</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows 8 Professional</td>
<td>NG4HW-VH26C-733KW-K6F98-J8CK4</td>
</tr>
<tr>
<td>Windows 8 Professional N</td>
<td>XCVCF-2NXM9-723PB-MHCB7-2RYQQ</td>
</tr>
<tr>
<td>Windows 8 Enterprise</td>
<td>32JNW-9KQ84-P47T8-D8GGY-CWCK7</td>
</tr>
<tr>
<td>Windows 8 Enterprise N</td>
<td>JMNMF-RHW7P-DMY6X-RF3DR-X2BQT</td>
</tr>
<tr>
<td>Windows Server 2012</td>
<td>BN3D2-R7TKB-3YPBD-8DRP2-27GG4</td>
</tr>
<tr>
<td>Windows Server 2012 N</td>
<td>8N2M2-HWPGY-7PGT9-HGDD8-GVGGY</td>
</tr>
<tr>
<td>Windows Server 2012 Single Language</td>
<td>2WN2H-YGCQR-KFX6K-CD6TF-84YXQ</td>
</tr>
<tr>
<td>Windows Server 2012 Country Specific</td>
<td>4K36P-JN4VD-GDC6V-KDT89-DYFKP</td>
</tr>
<tr>
<td>Windows Server 2012 Server Standard</td>
<td>XC9B7-NBPP2-83J2H-RHMBY-92BT4</td>
</tr>
<tr>
<td>Windows Server 2012 MultiPoint Standard</td>
<td>HM7DN-YVMH3-46JC3-XYTG7-CYQJJ</td>
</tr>
<tr>
<td>Windows Server 2012 MultiPoint Premium</td>
<td>XNH6W-2V9GX-RGJ4K-Y8X6F-QGJ2G</td>
</tr>
<tr>
<td>Windows Server 2012 Datacenter</td>
<td>48HP8-DN98B-MYWDG-T2DCC-8W83P</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows 7 and Windows Server 2008 R2</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows 7 Professional</td>
<td>FJ82H-XT6CR-J8D7P-XQJJ2-GPDD4</td>
</tr>
<tr>
<td>Windows 7 Professional N</td>
<td>MRPKT-YTG23-K7D7T-X2JMM-QY7MG</td>
</tr>
<tr>
<td>Windows 7 Professional E</td>
<td>W82YF-2Q76Y-63HXB-FGJG9-GF7QX</td>
</tr>
<tr>
<td>Windows 7 Enterprise</td>
<td> 33PXH-7Y6KF-2VJC9-XBBR8-HVTHH</td>
</tr>
<tr>
<td>Windows 7 Enterprise N</td>
<td>YDRBP-3D83W-TY26F-D46B2-XCKRJ</td>
</tr>
<tr>
<td>Windows 7 Enterprise E</td>
<td>C29WB-22CC8-VJ326-GHFJW-H9DH4</td>
</tr>
<tr>
<td>Windows Server 2008 R2 Web</td>
<td>6TPJF-RBVHG-WBW2R-86QPH-6RTM4</td>
</tr>
<tr>
<td>Windows Server 2008 R2 HPC edition</td>
<td>TT8MH-CG224-D3D7Q-498W2-9QCTX</td>
</tr>
<tr>
<td>Windows Server 2008 R2 Standard</td>
<td>YC6KT-GKW9T-YTKYR-T4X34-R7VHC</td>
</tr>
<tr>
<td>Windows Server 2008 R2 Enterprise</td>
<td>489J6-VHDMP-X63PK-3K798-CPX3Y</td>
</tr>
<tr>
<td>Windows Server 2008 R2 Datacenter</td>
<td>74YFP-3QFB3-KQT8W-PMXWJ-7M648</td>
</tr>
<tr>
<td>Windows Server 2008 R2 for Itanium-based Systems</td>
<td>GT63C-RJFQ3-4GMB6-BRFB9-CB83V</td>
</tr>
</tbody>
</table>
<h5 class="ml-3 mt-3">Windows Vista and Windows Server 2008</h5>
<table class="table table-hover ">
<thead>
<tr>
<th scope="col">Operating System</th>
<th scope="col">KMS Activation Serial Number</th>
</tr>
</thead>
<tbody>
<tr>
<td>Windows Vista Business</td>
<td>YFKBB-PQJJV-G996G-VWGXY-2V3X8</td>
</tr>
<tr>
<td>Windows Vista Business N</td>
<td>HMBQG-8H2RH-C77VX-27R82-VMQBT</td>
</tr>
<tr>
<td>Windows Vista Enterprise</td>
<td>VKK3X-68KWM-X2YGT-QR4M6-4BWMV</td>
</tr>
<tr>
<td>Windows Vista Enterprise N</td>
<td>VTC42-BM838-43QHV-84HX6-XJXKV</td>
</tr>
<tr>
<td>Windows Web Server 2008</td>
<td>WYR28-R7TFJ-3X2YQ-YCY4H-M249D</td>
</tr>
<tr>
<td>Windows Server 2008 Standard</td>
<td>M24T-X9RMF-VWXK6-X8JC9-BFGM2</td>
</tr>
<tr>
<td>Windows Server 2008 Standard without Hyper-V</td>
<td>W7VD6-7JFBR-RX26B-YKQ3Y-6FFFJ</td>
</tr>
<tr>
<td>Windows Server 2008 Enterprise</td>
<td>YQGMW-MPWTJ-34KDK-48M3W-X4Q6V</td>
</tr>
<tr>
<td>Windows Server 2008 Enterprise without Hyper-V</td>
<td>39BXF-X8Q23-P2WWT-38T2F-G3FPG</td>
</tr>
<tr>
<td>Windows Server 2008 HPC</td>
<td>RCTX3-KWVHP-BR6TB-RB6DM-6X7HP</td>
</tr>
<tr>
<td>Windows Server 2008 Datacenter</td>
<td>7M67G-PC374-GR742-YH8V4-TCBY3</td>
</tr>
<tr>
<td>Windows Server 2008 Datacenter without Hyper-V</td>
<td>22XQ2-VRXRG-P8D42-K34TD-G3QQC</td>
</tr>
<tr>
<td>Windows Server 2008 for Itanium-Based Systems</td>
<td>4DWFP-JF3DJ-B7DTH-78FJB-PDRHK</td>
</tr>
</tbody>
</table>


### Server yang tersedia
- Main   **kms.iqbalrifai.eu.org**.
- Luxembourg **kms.lux.iqbalrifai.eu.org**.
- Korea Selatan  **kms.kor.iqbalrifai.eu.org**.

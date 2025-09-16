[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/tPVgLsdF)

| Name | NRP | Class |
| Muhammad Ari Fathan Mahardika | 5025241013 | Jaringan Komputer (IUP) |


## Task 1

- Flag

  `JARKOM25{Ja0G_Bbbb4ng3t_S1_ZGKWT7TDW2HUBOZ0SW0767KRIH3K1N0xl0vel1zb6adtppt15dabwxw1a6bb8_844196915f455811c800a93b142c220a}`

> a. Berapa banyak packet yang terekam pada file pcapng?

> _a. How many packets are recorded in the pcapng file?_

**Answer:** `9596`

- Filter expression

  `-`

- Explanation

  `Using 'Capture File properties' to see how many packet recorded `

- Output result
<br>
**Wireshark**


![](https://github.com/user-attachments/assets/07b121b7-34f3-41f8-8767-90f603c1acc7)



**Terminal**
![](https://i.imgur.com/Z9VsOAv.png)


<br>
<br>

> b. Ada berapa jenis protocol (total) yang terekam pada traffic?

> _b. How many types of protocol (totals) are recorded in the traffic?_

**Answer:** `12`

- Filter expression

  `-`

- Explanation

  `Using 'protocol Hierarchy' to see how many  types of protocol`

- Output result
<br>
**Wireshark**
  ![](<img width="1361" height="550" alt="image" src="https://github.com/user-attachments/assets/702c6055-66e2-497b-a8b0-d6878ab9be3d" />
)
  **Terminal**
![](https://i.imgur.com/Z9VsOAv.png)

<br>
<br>

> c. Ada berapa jenis protocol berbasis TCP yang terekam pada traffic?

> _c. How many types of TCP-based applications protocol are recorded in the traffic?_

**Answer:** `8`

- Filter expression

  `-`

- Explanation

  `Using 'protocol Hierarchy' to see how many  TCP-based applications protocol are recorded in the traffic?`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/pl10AY9.png)
  **Terminal**
![](https://i.imgur.com/Z9VsOAv.png)


  <br>
  <br>

> d. Ada berapa banyak packet dengan protokol TCP murni yang terekam pada traffic (tanpa data)?

> _d. How many packets with pure TCP protocol are recorded in the traffic (without data)?_

**Answer:** `3223`

- Filter expression

  `-`

- Explanation

  `Using 'protocol Hierarchy' to see how many packets with pure TCP protocol are recorded in the traffic (without data)?_`

- Output result
<br>
 **Wireshark**
  ![](https://i.imgur.com/pl10AY9.png)
  **Terminal**
![](https://i.imgur.com/Z9VsOAv.png)

## Task 2

- Flag

  ` JARKOM25{N1c3_0ne_b4nggg_ZEQRJFMTHEyuMM13yrltqpbnfnkjstifhtudlc3r4t0ps08222419556422972710_0d22e8ac4d8736db1c9e1eb64353a818}`

> a. Berapa banyak packet berhasil yang berbasis murni TCP dan memiliki flag [ACK]?

> _a. How many packets succeed that are pure TCP based and have [ACK] flag?_

**Answer:** `3209`

- Filter expression

  `tcp.len == 0 && tcp.flags.ack == 1`

- Explanation

  `To filter the pure tcp ( Without data ) and to filter tcp with ack flags. And we can see one “TCP ACKed unseen segment” `

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/vaFTsNQ.png)
  **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/xm0CiPs.png)

  <br>
  <br>

> b. Berapa banyak packet berhasil yang berbasis murni TCP yang hanya memiliki flag [ACK]?

> _b. How many packets succeed that are pure TCP based and have only [ACK] flag?_

**Answer:** `3172`

- Filter expression

  `tcp.len == 0 && tcp.flags.ack == 1 && tcp.flags.syn == 0 && tcp.flags.fin == 0 && tcp.flags.reset == 0 `

- Explanation

  `To see only the pure tcp and have only the ack flags by making the other flag zero. After that we got 3174 becuase there are two “TCP ACKed unseen segment” `

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/0M7oV75.png)
    **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/xm0CiPs.png)

  <br>
  <br>

> c. Berapa banyak packet berhasil yang berbasis murni TCP dan memiliki flag selain hanya [ACK]?

> _c. How many packets succeed that are pure TCP based and contain flags other than just [ACK] flag?_

**Answer:** `49`

- Filter expression

  ``

- Explanation

  `We can see the all packets with pure TCP is 3223 and with ack file is 3172 and we can get the result is 51. But there are two TCP ACKed unseen segment” ` 

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/l9t8gso.png)
  ![](https://i.imgur.com/l9t8gso.png)

    **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/xm0CiPs.png)

  <br>
  <br>

## Task 3

- Flag

  `JARKOM25{W0w_Y0uU_h4V33e_d0n3_444_90od_j0bB_3100Og0dl1k347y106kcd2vvmlqbnowdzj_ce2333fae101c6fb04afbf45f7fba3ef}`

> a. Pada port berapa client telnet terbuka?

> _a. In what port is the telnet client open?_

**Answer:** `54184`

- Filter expression

  `telnet`

- Explanation

  `Just search telnet to see the telnet client, and we can see in S`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/s5zRRio.png)
      **Terminal**
  ![](https://i.imgur.com/fc2sBxb.png)

  <br>
  <br>

> b. Berapa byte file response yang dikirim dari server?

> _b. How many bytes of the response files are sent from the server?_

**Answer:** `1449`

- Filter expression

  `telnet`

- Explanation

  `Just filter telnet and follow one of the stream and we can see at file response file in bytes. And after that we can see thar the total bytes is 1449 bytes`

- Output result
<br>
  **Wireshark**
  ![](https://i.imgur.com/q64nQK5.png)
      **Terminal**
  ![](https://i.imgur.com/fc2sBxb.png)

  <br>
  <br>

> c. Apa username yang digunakan client telnet untuk berhubungan dengan server?

> _c. What telnet client's username is used to connect with the server?_

**Answer:** `jovyan`

- Filter expression

  `telnet`

- Explanation

  `Just follow one of the telnet filter and follow the tcp stream and we can see the username`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/VHlFAJT.png)
    **Terminal**
  ![](https://i.imgur.com/fc2sBxb.png)

  <br>
  <br>

> d. Apa password client telnet?

> _d. What is the telnet client's password?_

**Answer:** `123`

- Filter expression

  `telnet`

- Explanation

  `Just follow one of the telnet filter and follow the tcp stream and we can see the password`

- Output result
<br>
  **Wireshark**
  ![](https://i.imgur.com/VHlFAJT.png)

  **Terminal**
  ![](https://i.imgur.com/fc2sBxb.png)

  <br>
  <br>

## Task 4

- Flag

  `JARKOM25{G04t__a4n4liz333er_1S8DGVSXLS1GOTSC7WB7fr0g28saecqk6gnnostr3ys1614513394_ad11e46f218efb128d3325885208db77}`

> a. Apa perintah pertama yang ditulis client pada koneksi telnet?

> _a. What is the first command that client wrote on telnet connection?_

**Answer:** `echo`

- Filter expression

  `telnet`

- Explanation

  `To filter with the telnet connection we use telnet. And follow the TCP stream. After that we can scroll down to see the first command is 'echo'`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/A9DDsLd.png)
    **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/pUXrHaw.png)

  <br>
  <br>

> b. Apa nama file .txt di server (ditulis bersama ekstensinya)?

> _b. What is the name of .txt file on the server (write with the extension)?_

**Answer:** `test.txt`

- Filter expression

  `telnet`

- Explanation

  `To filter with the telnet connection we use telnet. And follow the TCP stream. After that we can find the stream by using find "txt"`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/1TTTPfk.png)
    **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/pUXrHaw.png)

  <br>
  <br>

> c. Apa kata pertama dari frasa yang dimasukkan client ke dalam file sebelumnya?

> _c. What is the first word that the client inserted into the previous file?_

**Answer:** `jarkom`

- Filter expression

  `telnet`

- Explanation

  `To filter with the telnet connection we use telnet. And follow the TCP stream. After that we can find the stream by using find echo, and we can scroll down to see the first word that client inserted`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/AIplbSW.png)
    **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/pUXrHaw.png)

  <br>
  <br>

## Task 5

- Flag

  `JARKOM25{n4il0ng_m1lk_dr4g000n_CMYLGCWNMC269FJ4AMH9UBOJCUQ5WZcr0ch05qxuz639nwmyyyxc4db434_fc13a45e522158d392e4137fbe61b883}`

> a. Berapa banyak packet berbasis HTTP yang terekam pada file pcapng?

> _a. How many HTTP packets are recorded in the pcapng file?_

**Answer:** `298`

- Filter expression

  `http`

- Explanation

  `After we filter it with http, we can see the displayed http is 298`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/RjhTb0H.png)
     **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/PVbVs2h.png)

  <br>
  <br>

> b. Ada berapa HTTP packet yang berupa response?

> _b. How many response HTTP packets are recorded in the traffic?_

**Answer:** `149`

- Filter expression

  `http.response`

- Explanation

  `We can filter the HTTP one with additional 'response' to see all the HTTP response`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/KNOXNPV.png)
   **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/PVbVs2h.png)

  <br>
  <br>

> c. Ada berapa paket berbasis HTTP yang berhasil?

> _c. How many HTTP packets that succeed?_

**Answer:** `296`

- Filter expression

  `http`

- Explanation

  `We can filter it by seeing the http and we can see there are two TCP previous segment not captured`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/vtjmmZA.png)
   **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/PVbVs2h.png)

  <br>
  <br>

> d. Apa alamat IP dari client HTTP yang tersambung lokal dengan mesin lain?

> _d. What is the client HTTP IP Address in connection with other local machine?_

**Answer:** `172.16.16.101`

- Filter expression

  `http`

- Explanation

  `After we filter it by http, we can see the src or HTTP IP address that are in connection with the local machine is '172.16.16.101`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/vtjmmZA.png)
   **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/PVbVs2h.png)

  <br>
  <br>

## Task 6

- Flag

  `JARKOM25{br0mb44rdin0u_Cr0ccc0c0c0cdi1l10l_3081903627awaesa5mq88yjfm5sh1n0buDKL7DSM6GJ6U3WZ_4840e1bc4e2da0a654005c29d7e56e5f}`

> a. Apakah kamu menemukan fake flag? Tuliskan seluruhnya!

> _a. Did you find the fake flag? Write it whole!_

**Answer:** `FakeFlag{JarkomGampang}`

- Filter expression

  `CTRL + F,and then search 'flag'`

- Explanation

  `Using the search filter and search flag. After that we choose the HTTP stream. By that we can see the fake flag`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/9Mez1mx.png)
   **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/CXgefLr.png)

  <br>
  <br>

> b. Tuliskan username dan password yang tertulis! (format username:password)

> _b. Write the written username and password! (format username:password)_

**Answer:** `Rey:123`

- Filter expression

  `HTTP and Ctrl + F "pass"`

- Explanation

  `If we want to see the username and password we cans search it by see the username and password in the string`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/XVykxfj.png)
   **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/CXgefLr.png)
  <br>
  <br>

## Task 7

- Flag

  `JARKOM25{tr4l4lel0_tr1lil1_drm0p86wlek3b0s0sCTP0WLH3YFXLNO7_bc0b18a40a047554a3618f1527e53822}`

> Apa nama gambar yang direquest oleh client? (tulis dengan ekstensinya)

> _What is the image that is being requested by the client? (write with its extension)_

**Answer:** `donalbebek.jpg`

- Filter expression

  `HTTP. CTRL + F "jpg"`

- Explanation

  `If we want to see the image that requested by the client we have to filter it using HTTP to filter the connection that request a website. After that we know commonly picture in the website in a jpg format. So we can see in the picture it mentioned 'donalbebek.jpg'. Afterwards we can see the below website send the picture that already requested`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/ItJfd1I.png)
     **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![alt text](https://i.imgur.com/SFxhjfZ.png)

  <br>
  <br>

## Task 8

- Flag

  `JARKOM25{y0u_4r3_s0_G00d_1n_F0r3nsic_2C517T3I4D9WOFY4BZASED7DB1AYD1x45y4n6jtz2nhcdbznbp22qero8aa9_81b18d1b362bc32dc1f035c0495a9800}`

> a. Berapa banyak packet berbasis FTP yang terekam pada file pcapng? (with the data)

> _a. How many FTP packets are recorded in the pcapng file? (with the data)_

**Answer:** `81`

- Filter expression

  `ftp || ftp-data`

- Explanation

  `We can see the filter FTP is for the FTP package with an addition FTP data because the question is asked to do so`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/DWRLt97.png)
   **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/cOtCgwV.png)

  <br>
  <br>

> b. Apa username dan password client di koneksi FTP? (tulis dalam format username:password)

> _b. What is the client's username and password in FTP connection? (write in following format username:password)_

**Answer:** `rey:password123lingangu`

- Filter expression

  `successful`

- Explanation

  `To see the client's username and password in FTP by see the client who succes login, so we can search it by search by the find tools that provided by wireshark and search 'successful`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/Pofq015.png)
     **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/cOtCgwV.png)

  <br>
  <br>

> c. What is the client's command for showing server directory that was sent on request packet?

> _c. Apa command client untuk melihat direktori server yang dikirimkan dalam request packet?_

**Answer:** `LIST`

- Filter expression

  `successful`

- Explanation

  `We can see the clients send the command LIST to see all the directory server for the FTP `

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/Pofq015.png)
       **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/cOtCgwV.png)

  <br>
  <br>

## Task 9

- Flag

  `JARKOM25{j4rk000000mmm_g4mpp4444n9999999_71584114818i41L4hjzrjjv88vh321k0ncolX2PL7JCT2EURWXE_bbb445a9acce5084d04d7c2f3d8169d9}`

> a. Apa alamat IP dari FTP server?

> _a. What is the FTP server IP Address?_

**Answer:** `172.16.16.101`

- Filter expression

  `ftp`

- Explanation

  `Imagine two people are talking: one asks (the client), and one answers (the server).In the capture, the answers like “Welcome” and “Login successful” always come from 172.16.16.101.`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/NTRysqL.png)
  **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/xaFex5A.png)

  <br>
  <br>

> b. Berapa banyak file yang ada dalam direktori FTP server?

> _b. How many files are there inside the FTP server directory?_

**Answer:** `7`

- Filter expression

  `ftp`

- Explanation

  `We can check it by seeing the following tcp stream untul we see the files inside the FTP server`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/zU5jMZc.png)
    **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/xaFex5A.png)


  <br>
  <br>

> c. Apa nama dari file yang digunakan dalam page.html? (tulis lengkap namanya beserta ekstensinya dan dipisahkan dengan koma ',')

> _c. What are the filenames used in the page.html? (write the filebames with their extensions and separate them with comma ',')_

**Answer:** `pokijan.jpg,research_center.jpg`

- Filter expression

  `tcp`

- Explanation

  `We follow the tcp stream one by one and we can see the one with the form of HTMl and we can see there are pokijan and research center in the form of jpg`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/H6xVn15.png)
   **Terminal ( Sorry i forgot to Screenshoot, but i already copy paste all my command in Mincrosoft Word)**
  ![](https://i.imgur.com/xaFex5A.png)

  <br>
  <br>

## Task 10

- Flag

  ` JARKOM25{f1nisssshs55s5s533s_l1n333ee333E3_07882644732910qnekjnaext345215123123PUC11ST69KID4UE_7785589ced88a7ac3ba54f292f4bf82f}`

> a. Apa nama file yang mengandung string terencode?

> _a. What is the filename that contains encoded string?_

**Answer:** `secret.txt`

- Filter expression

  `tcp contains ".txt"`

- Explanation

  `We can see usually file to keep some encoded string is in a txt file. In addition we can see the file is in the name of 'secret.txt'. It's to prove it some secret stuff with encoded string or we need some additional tools so we can understand it in human language or decoded it`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/mbMhTxz.png)
  **Terminal**
![](https://i.imgur.com/C0URwIt.png)

  <br>
  <br>

> b. Apa nama file hasil copy file sebelumnya?

> _b. What is the filename of the previous file copy?_

**Answer:** `secret1.txt`

- Filter expression

  `tcp contains ".txt"`

- Explanation

  `We can see if we want to copy some file we can not name it in the exactly same name, so we have to rename it. Thus secret1 is almost precisely the same as secret.txt. So we know is the copy form of "secret.txt"`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/mbMhTxz.png)

  **Terminal**
![](https://i.imgur.com/C0URwIt.png)

  <br>
  <br>

> c. What is the decoded string from the previous file?

> _c. Apa decoded string dari file tersebut?_

**Answer:** `Pada suatu hari Rey bertemu dengan Nailong the Milk Dragon. Ketika bertemu, Rey mengajarkan Nailong apa itu Jaringan Komputer. Nailong pun senang karena ternyata Jaringan Komputer itu gampang.`

- Filter expression

  `TCP and using the base 64 `

- Explanation

  `We can see the encode file and we can using the base 64 to decoded the string into some human language that we can understand`

- Output result
<br>
**Wireshark**
  ![](https://i.imgur.com/mbMhTxz.png)
**Base 64**
![](https://i.imgur.com/tp2kxbL.png)

**Terminal**
![](https://i.imgur.com/C0URwIt.png)

  <br>
  <br>

## Summary
- You analyzed a multi-protocol pcapng and extracted three flags across tasks 1–10 using Wireshark features: Capture File Properties, Protocol Hierarchy, Display Filters, and Follow TCP Stream.

- You correctly counted total packets (9,596), protocol families (12 total; 8 TCP-based apps), and identified pure TCP packets (no payload) and their flag breakdown (ACK-only vs. others).

- For application layers, you verified HTTP packet totals and “success” adjustment (excluding 2 flows with missing segments), and for TELNET you retrieved port, response size, username, password, and first commands.

- For FTP, you identified the server IP, enumerated files in the directory, recognized the LIST command, and extracted credentials.

- In Task 10, you found the encoded file (secret.txt), its copy (secret1.txt), and correctly decoded the Base64 string to readable Indonesian text.

## Problems

## Problems

- Some filters were too general (e.g., searching “successful” instead of using exact FTP fields).  
- ACK-only filter was incomplete (did not exclude PSH/URG/ECE/CWR flags).  
- Counts were adjusted because of “TCP ACKed unseen segment,” which is just a capture issue.  
- HTTP “success” definition was unclear (needed explanation why 298 → 296).  
- Possible confusion between client and server IP roles (e.g., 172.16.16.101).  
- Explanations were sometimes too long or unclear.  
- Some screenshots were missing (not all outputs shown in Wireshark).  


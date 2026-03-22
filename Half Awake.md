## Step 1)
I first opened the file in wireshark and check for any flag-related strings in the streams.
## Step 2)
Since none of the streams showed anything, I went over to check the conversations and went through the UDP streams
## Step 3)
One of the conversations was from a different initial address, so I went followed that stream and it had some hints, which said to investigate the mDNS streams, to loads having PK and to check up on the TCP blobs closely
<img width="954" height="611" alt="Screenshot 2026-03-22 214827" src="https://github.com/user-attachments/assets/d3cfdda7-e631-4fc0-83bc-a5ba895157c0" />
## Step 4)
I went through 2nd stream and found stage2.binPK and readme.binPK. I binwalked the pcap file and found and went through both of them. The readme file said "not everything here is encrypted the same way" and the stage2bin file gave: 
ufa{4fa43s3t3p000_rc} 
which looked similar to the flag, but was missing alterante letters.
## Step 5)
While going through other convos in the UDP stream, I found below hints
<img width="1256" height="846" alt="image" src="https://github.com/user-attachments/assets/f8e9eb6e-0a7d-479e-9c8c-a9978b7696cf" />
Here, alert chunk may be telling to go trough chunks, Chef decode may refer to cyberchef, and key version may be key for XOR
## Step 6)
Since all odd letters were present, but even were absent, the even positions could be obtained by XOR'ing the obtained flag with different keys until alternate letters from initial part came (like 't', 'l', 'g'). On doing so, I obtained tlghl_wk_3_h_rtclt1k
On combining both, we get:
utflag{h4lf_aw4k3_s33_th3_pr0t0c0l_tr1ck}




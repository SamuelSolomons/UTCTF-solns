## Step 1)
I first opened the file in wireshark and check for any flag-related strings in the streams.
## Step 2)
I went over to the TCP streams, but none of them showed anything different. So I went over to the UDP streams and found 3 streams which had much highe byte transfers
(pic)
## Step 3)
On following their streams, I found some text and 0s or 1s after them, which meant that this must be binary data
(pic)
## Step 4)
The first 2 streams did not give any useful data when 0s and 1s were filtered and decrypted, but the third stream gave :
utflag{d1g_t0_th3_l4st_byt3}
(pic)





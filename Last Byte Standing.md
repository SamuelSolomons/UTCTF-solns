## Step 1)
I first opened the file in wireshark and check for any flag-related strings in the streams.
## Step 2)
I went over to the TCP streams, but none of them showed anything different. So I went over to the UDP streams and found 3 streams which had much highe byte transfers
<img width="1452" height="61" alt="Screenshot 2026-03-22 224522" src="https://github.com/user-attachments/assets/1628fc36-3864-4c7f-9895-81c2ddb8d92d" />
## Step 3)
On following their streams, I found some text and 0s or 1s after them, which meant that this must be binary data
<img width="1277" height="1016" alt="image" src="https://github.com/user-attachments/assets/792b40d5-3c1c-4751-9d76-79c314fc2fdd" />
## Step 4)
The first 2 streams did not give any useful data when 0s and 1s were filtered and decrypted, but the third stream gave :
utflag{d1g_t0_th3_l4st_byt3}
<img width="1593" height="841" alt="Screenshot 2026-03-22 225330" src="https://github.com/user-attachments/assets/30393c9c-21e7-4de7-83d7-2887617184bf" />






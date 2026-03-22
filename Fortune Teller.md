## Step 1
I first recovered a and c and then subtractecd consecutive recurrence equations to cancel  c
a = (x3 - x2) * modinv(x2 - x1, m) mod m
c = (x2 - a * x1) mod m
a = 3355924837, c = 2915531925.

## Step 2:
I then computed output 5
output_5 = (a * x4 + c) mod 2^32 = 1233863684

## Step 3: 
I then took output_5 as key, XOR'ed it cyclically with the ciphertext:

key = 0x498b4404
flag = ciphertext XOR key (repeating)
Flag: utflag{pr3d1ct_th3_futur3_lcg}






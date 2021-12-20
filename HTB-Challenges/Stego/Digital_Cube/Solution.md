# [Digital Cube](https://app.hackthebox.com/challenges/digital-cube)

Stego challenge

## Requirements

[dcode](https://www.dcode.fr/binary-image)

## Solution

- Unzip with

    ```
    unzip Digital\ Cube.zip
    ```
- See what the .txt contains
    
    ```
    cat digitalcube.txt
    ```
    
    and we get binary representation.
 
- We try to find what is representing. We check for an image at

  [dcode](https://www.dcode.fr/binary-image)
  
  and as for the image size we know from the challenge description 50:50.
  
- A QRCode appears. We scan it with a phone and we get the flag.

- Flag: HTB{QR_!snt_d34d}
    
   

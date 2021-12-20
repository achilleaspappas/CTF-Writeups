# [Pusheen Loves Graphs](https://app.hackthebox.com/challenges/pusheen-loves-graphs)

Stego challenge

## Requirements

[IDA](https://hex-rays.com/ida-free/)

## Solution

- Change the permission with 

    ```
    chmod +x Pusheen
    ```
 
 - Try to execute
 
    ```
    ./Pusheen 
    ```
    
    And we only get an image of a cat.

- As we know Pusheen loves graphs and only likes the IDA. So we open it with IDA and choose graph overview.

- The flag reveals itself when we see the overview.

- Flag: HTB{fUn_w17h_CFGz}

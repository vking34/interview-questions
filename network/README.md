# Network

## TCP Handshake Flow
1. Client send TCP SYN to Server
2. Server send TCP SYN + ACK back to Client
3. Client send TCP ACK

## SSL/TSL Handshake Flow

1. TCP handshake between Client and Server
2. Server send Public Key to Client
3. Client generate Session Key then Session Key is encrypted by Public Key
4. Client send the encrypted Session Key to Server. Server decrypt to get Session Key
5. Client & Server transfer data using Session Key

Using Session Key is asymmetric mechanism that reduces resources to encrypt/decrypt data






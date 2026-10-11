# TFTP-Client-Server
Implemented a TFTP client-server application in C using UDP socket programming in Linux for file upload and download, with packet handling and error management.

# TFTP Client-Server Implementation

## Description

Developed a Trivial File Transfer Protocol (TFTP) client-server application in C using UDP socket programming in Linux. The project supports file upload and download through request, data, acknowledgment, and error packets.

## Features

- File upload and download
- UDP-based client-server communication
- Read Request (RRQ) and Write Request (WRQ)
- DATA, ACK, and ERROR packet handling
- Block-wise file transfer
- Error handling for file transfer operations

## Technologies Used

- C Programming
- Linux
- UDP Socket Programming
- File I/O
- TFTP Protocol (RFC 1350)

## Protocol Overview

TFTP uses UDP to transfer files between a client and a server.

| Opcode | Packet Type         |
| ------ | ------------------- |
| 1      | Read Request (RRQ)  |
| 2      | Write Request (WRQ) |
| 3      | DATA                |
| 4      | ACK                 |
| 5      | ERROR               |

Data is transferred in blocks of up to 512 bytes, with block numbers and acknowledgments used to manage the transfer.

## Commands

- `connect <ip>` – Connect to the server
- `get <filename>` – Download a file
- `put <filename>` – Upload a file
- `mode <octet/netascii>` – Set transfer mode, if implemented
- `bye` or `quit` – Exit the client

## Compilation

Compile the client and server source files using GCC:

```bash
gcc client.c -o client
gcc server.c -o server
```

## Execution

1. Start the server:

   ```bash
   ./server
   ```

2. Start the client in another terminal:

   ```bash
   ./client
   ```

3. Connect to the server and use the supported commands to upload or download files.

##


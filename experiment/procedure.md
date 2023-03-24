### Procedure

1.  Begin a session by typing the following command on terminal 1 with the server's IP address and port. 
    - openssl s_client -connect host:port

2. On a successful connection, the server will send a copy of its assymmetric public key to the client. Try catting the file to see what it looks like.
    - cat server_pubkey.pem

3. The client then creates a static session key by executing the following command.
    - openssl rand -hex 16 > sessionkey.txt

4.  The client then encrypts the session key using the server's public key.
    - openssl rsautl -encrypt -in sessionkey.txt -out sessionkey.enc-pubin -inkey server_pubkey.pem

5. The client then sends the encrypted session key to the server.
    - cat sessionkey.enc | nc host port

6. The server then decrypts the session key using its private key.
    - openssl rsautl -decrypt -in sessionkey.enc -out sessionkey.txt -inkey server_privkey.pem

7. The server has decrypted the session key using its private key. Try catting the file to see what it looks like, it should be the same as the session key generated in step 3.

8. To identify the host IP, the client will send a ping request to the server by executing the following command:
    - ping -c 3 IP_ADDRESS

9. To display the certificate info of the server, the client will execute the following command:
    - openssl x509 -in server.crt -text -noout

10. To quit the session, the client will execute the following command:
    - quit


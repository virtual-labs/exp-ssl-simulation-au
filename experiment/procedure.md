### Procedure

1. Student need to copy the command(“openssl s_client -connect host:port”) by single clicking it  and paste in the terminal.

2. Change the host to the given server's IP address and port to the given port no and click enter.

3. Observe the “CONNECTED” message in the terminal now the session has started. In case of an unacceptable command sequence, the server responds with “Invalid Command”.

4. On a successful connection, the server will send a copy of its asymmetric public key file to the client.

5. Copy the command(“cat server_pubkey.pem”) paste in the terminal.

6. Observe how the asymmetric public key file looks like.

7. Copy the command(“openssl rand -hex 16 > sessionkey.txt”) paste in the terminal and click enter.

8. Observe the client creating a static session key.

9. Copy the command(“openssl rsautl -encrypt -in sessionkey.txt -out sessionkey.enc -pubin -inkey server_pubkey.pem”) paste in the terminal and click enter.

10. Observe the client encrypting the session key using the server's public key.

11. Copy the command(“cat sessionkey.enc | nc host port”) paste in the terminal.

12. Change the host to the given server's IP address and port to the given port no and click enter.

13. Observe the client sending the encrypted session key to the server and the terminal being switched from client to server.

14. Copy the command(“openssl rsautl -decrypt -in sessionkey.enc -out sessionkey.txt -inkey server_privkey.pem”) paste in the terminal and click enter.

15. Observe the server decrypting the session key using its private key and saving it to sessionkey.txt.

16. Copy the command(“ping -c 3 IP_ADDRESS”) paste in the terminal.

17. Change the IP_ADDRESS to the given ip address.

18. Observe the client sending a ping request to the server to identify the host IP.

19. Copy the command(“openssl x509 -in server.crt -text -noout”) paste in the terminal and click enter.

20. Observe the certificate information of the server.

21. Copy the command(“quit”) paste in the terminal and click enter.

22. Observe the session being quit.

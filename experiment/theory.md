### Theory

SSL (Secure Sockets Layer), now known as TLS (Transport Layer Security), is a protocol for encrypting and securing data transmitted over the internet. It provides a secure and encrypted channel between a client (such as a web browser) and a server, ensuring that data transmitted over the internet cannot be intercepted or tampered with by third parties.

When an SSL/TLS connection is established between a client and server, the data transmitted between them is encrypted using a cryptographic key. This key is generated during the SSL/TLS handshake process and is known only to the client and server.

SSL/TLS also provides authentication, which ensures that the client is communicating with the intended server and not an impostor. This is done by verifying the server's digital certificate, which contains information about the server's identity and public key. The client can use this information to ensure that it is communicating with a legitimate server.

Here is how SSL/TLS works:

1. **Client Hello:** The client initiates the SSL/TLS connection by sending a `ClientHello` message to the server. This message contains information about the client's SSL/TLS capabilities, such as the version of SSL/TLS supported, cipher suites, and compression methods.

2. **Server Hello:** The server responds with a `ServerHello` message, which includes the SSL/TLS version, a cipher suite, and a server certificate. The server certificate contains a public key that the client can use to encrypt data before sending it to the server.

3. **Client Authentication:** If the server requires client authentication, it will send a request for a client certificate. The client will then send its certificate to the server for verification.

4. **Key Exchange:** The client and server exchange information to establish a shared secret key. This key will be used to encrypt and decrypt data during the SSL/TLS session.

5. **Session Key:** The client and server generate a session key that will be used to encrypt data transmitted during the SSL/TLS session.

6. **Data Exchange:** Once the session key is established, data can be transmitted securely between the client and server. All data transmitted between the two parties is encrypted using the session key.

7. **Connection Closure:** When the SSL/TLS session is complete, either the client or server can initiate the connection closure. The SSL/TLS connection is closed gracefully, with both parties sending a message to indicate that the connection is being closed.

Overall, SSL/TLS provides a secure and encrypted channel for transmitting sensitive data over the internet, such as credit card numbers, login credentials, and other personal information. It is widely used to secure online transactions, e-commerce, online banking, and other sensitive communications.

# local-server

Establishing local server USING NODE.js
: Two PEM (printable encoded archive) files are attached
   1. cert.pem : this file helps to verify the authenticity of the main file.
   2. key.pem  : this file enables to activate the local server using SSH hub.

How to Use:
#Generate self-signed certificate, follow this command:
$openssl genrsa -out key.pem
$openssl req -new -key key.pem -out csr.pem
$openssl x509 -req -days 9999 -in csr.pem -signkey key.pem -out cert.pem
$rm csr.pem

>> For Linux/Unix
Install npm

>> run command "node main.js"
>> open preferred browser
>> see the server running on preferred port.



apex-wsfederation
=================

ws-federation implementation in Apex

To get started:

1. Install this package ( https://login.salesforce.com/packaging/installPackage.apexp?p0=04ti00000008bvz ), or create the code from the Apex, and Pages directory, plus the required custom object 
2. Adjust CRUD and FLS 
3. Generate encoded keys / certs, follow the cryptocommands in the Keys directory.   When asked for a password, use something consistent for each answer.   Run the 5 commands and you'll end up with key.pem, which is your encodedPrivateKey ( protect this!! ), wsfed.crt which is your public certificate, and your modulus / exponent
4. You need to get just the base64 from the cert and the key and remove all line breaks
5. Go to /apex/WSFederationManagement and create a Realm

Now, you can authorize access to the WSFederation page via Profiles or Permsets and it will speak WSFed Passive profile

Consult this wiki for example intructions with Sharepoint: [https://developer.salesforce.com/page/Configuring-SSO-to-SharePoint]
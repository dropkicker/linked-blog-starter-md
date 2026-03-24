Ports Open: 80, 22
#webserver

Webserver. Running Metabase.  Clicked login page which showed a subdomain.  
Fed requests into Burp just for information/recon.

Checked version of Metabase, it was a vulnerable version per google.

Blogpost on vuln detailed a request payload(PUT) that we could gain RCE on the server.

The encoded command on the request included a base64 encoded command that created a reverse shell to a netcat listener we had running.

Checked env variables by running env 

It had a pw and username

Ssh'd into the user.

Low Priv.

Priv escalate by checking the kernal version.  The kernal was vulnerable to Gameoverlay exploit, easy one liner to put into low priv terminal and we're root!
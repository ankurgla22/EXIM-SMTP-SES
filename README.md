# SMTP-SES
Docker SMTP and SES image

1. Clone the docker file and exim configuration file.
2. Update the AWS SES authentication


 <pre>
begin authenticators
ses_login:
	driver = plaintext
	public_name = LOGIN
	client_send = : AKIAJ********747A : AvZzIpH*********lIvBzEG

 </pre>
3. Build the docker image

4. Run the exim container
 <pre>
$ docker run --name=exim  --restart=always -d -p 172.17.0.18:25:25 -e PRIMARY_HOST="Host-name" -e ALLOWED_HOSTS="*" ankurgla22/exim-ses
 </pre>
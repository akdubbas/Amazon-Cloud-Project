# Cloud Computing Project

Amazon Web Services(AWS)

Hosted Ubuntu WebServer 16.04 LTS (HVM) 64-bit on Amazon EC2 intance AWS, which provides HTTP and HTTPS application to operate on user entered data, and providing the result.

The Web Application is hosted on Web Server.

- Implemented a simple algorithm that takes a user input and returns a result that is derived from operating on that input
- Provides a form to accept user input using the GET method.
- Utilize one included file that is separate from the main application (such as a
CSS stylesheet) 



AIM: The Application takes the given input and finds the nth Fibonacci number in the series. When the user clicks on find button, the application displays the correct answer.

TECHNOLOGIES USED:

HTML/CSS/BOOTSTRAP are used for the front end and styling. python 2.7 was used for processing

index.html - the html file to receive the single number as input.

Style.css - to add styling to input.html file.

Installing nginx server

pip install nginx;

add the web-configuration at /etc/nginx/sites-enabled/nginx.conf;

sudo /etc/init.d/nginx start;

pip install gunicorn;

gunicorn --bind 0.0.0.0:8000 nameofyourapp.wsgi in project folder;

sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/cert.key -out /etc/nginx/cert.crt

Update nginx Config file with the below script

server {

listen *:443; ssl on; ssl_certificate cert.crt; ssl_certificate_key cert.key; ssl_session_timeout 5m; ssl_protocols SSLv3 TLSv1; ssl_ciphers ALL:!ADH:!EXPORT56:RC4+RSA:+HIGH:+MEDIUM:+LOW:+SSLv3:+EXP; ssl_prefer_server_ciphers on;

listen 80; return 301 https://$host$request_uri;

}

Reload nginx

HOW TO USE IT?

Click on the public https URL of the Application Click on 'ADVANCED' and then click on 'Proceed to 18.218.198.35 (unsafe)' The application should be running on https (Extra) Enter number in the input field provided Click on find button The application will display the nth number in the fibonacci series. LINKS: Public App URL: https://18.218.198.35
http://18.218.198.35



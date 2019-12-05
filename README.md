# NGINX VS APACHE Who's going to win?
Objetive expose same app that has the ability to sleep a request for X ms (https://www.npmjs.com/package/sleep-server).
Measure under the same conditions different webservers to determine which is faster

# Start web servers
`docker-compose up`

# Endpoints
* NGINX http://192.168.99.100:81/sleep/10000
* Apache http://192.168.99.100/sleep/10000

# Test (installing siege https://jasonmccreary.me/articles/installing-siege-mac-os-x-lion/)
`siege http://192.168.99.100:81/sleep/1000`

# Monitoring (live monitoring)
http://192.168.99.100:8080/

# Stop web servers
`docker-compose down`
Title: Use a web proxy for apt-get
Date: 2015-10-09 13:43
Tags: Linux

To configure using an HTTP proxy for apt-get, add the following line to your **/etc/apt/apt.conf** file (you may need to create the file)

`Acquire::http::Proxy "http://PROXY_HOST:PROXY_PORT";`

This will configure apt-get to use a web proxy without configuring it for the entire system. Just comment out or remove the line to reverse the change.

More information here:  
[https://help.ubuntu.com/community/AptGet/Howto#Setting_up_apt-get_to_use_a_http-proxy](https://help.ubuntu.com/community/AptGet/Howto#Setting_up_apt-get_to_use_a_http-proxy)
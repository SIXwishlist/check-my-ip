# check-my-ip

just put the index.php into a website, should work out of the box when browsing it.

i just had to make 2 changes in my /etc/services 

	echo "pptp        1723/tcp" >> /etc/services
	echo "rdp         3389/tcp" >> /etc/services

to use it just browse the page with you broweser.

in linux/bsd you can do something like this

using lynx:

	lynx -dump url-to-index.php

using curl:

	curl url-to-index.php -o testfileurl.htm
	awk '{gsub("<[^>]*>", "")}1' testfileurl.htm | sed 's/ //g' > testfileurl.txt && rm testfileurl.htm
	more testfileurl.htm

using links:

	links url-to-index.php


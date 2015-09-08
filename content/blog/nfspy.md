Title: NFSpy - Attacking NFS Servers
Date: 2015-09-06 22:35
Tags: Red Team, Tool, Security

I recently learned of the tool: [NFSpy](https://github.com/bonsaiviking/NfSpy) which can be used for attacking an NFS server.

	nfspysh -o server=<ip/host>:<dir>
	
	nfspysh -o server=192.168.12.41:/home/jimmy
# README #

Ansible playbook for haproxy and keepaliveD


* Deployment instructions

ansible-playbook -i inventory playbook.yaml

Summary
=======

This playbook installs haproxy and keepalived. With a host entry for domain my-google.com, it fetches the content of www.google.com , while retaining the URL as my-google.com 

For haproxy config manipulated HOST, X-Forwarded-Proto HTTP headers in the request. 

changed Location header in the response, so that upon receiving the response  the domain would be same my-google.com  in the URL bar.

ips used: 
vip      192.168.0.91
haproxy1 192.168.0.92
haproxy2 192.168.0.93


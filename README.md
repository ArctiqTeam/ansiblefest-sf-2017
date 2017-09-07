# Ansible for Networks: Beyond Static Config Templates
## AnsibleFest San Francisco 2017

This repository hosts the presentation and sample files used by Arctiq during our presentation at AnsibleFest San Francisco in 2017

Overall the idea was to showcase a multi-vendor network configuration that highlights the following:

 * Using Jinja2 templates and Ansible to build dynamic configuration templates and push them to network devices
 * Leveraging Jenkins and Git to trigger automation workflows (the same code used above) and build network deployment/validation pipelines

 Inside this repository you will find a copy of the presentation, and all of the code used in our demos.  Video demos to come in a followup Blog, as well as posted on Ansible's website following the event.

  * ansible folder - Ansible playbooks leveraging core network modules
  * ansible-napalm folder - Ansible playbooks leveraging the NAPALM abstraction library
  * Example Structure - Sample multi-vendor, multi-environment playbook structure

Any questions please contact:
@arctiqteam or @fairweathertim on Twitter or www.arctiq.ca

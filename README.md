# Requirements
If you have been doing the previous projects, you should already have a Linux server running. If not, setup a Linux server on DigitalOcean, AWS or another cloud provider.

You are required to write an Ansible playbook called setup.yml and create the following roles:

- base — basic server setup (installs utilities, updates the server, installs fail2ban, etc.)
- nginx — installs and configures nginx
- app — uploads the given tarball of a static HTML website to the server and unzips it.
- ssh - adds the given public key to the server

Set up the inventory file inventory.ini to include the server you are going to configure When you run the playbook, it should run the roles above in sequence. You should also assign proper tags to the roles so that you can run only specific roles.

Example:

```
# Run all the roles
ansible-playbook setup.yml

# Run only the app role
ansible-playbook setup.yml --tags "app"
```

[https://roadmap.sh/projects/configuration-management](https://roadmap.sh/projects/configuration-management)
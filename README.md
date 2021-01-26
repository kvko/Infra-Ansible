# Infra-Ansible

Infrastructure Automation with Ansible.

This project utilize ansible to provision server environment, and serve as a repository for `Jane` project deployment.

* User Account Management.
* Software Dependencies Management.
* Service Setup and Configuration.
* Project Deployment.


## Project layout
Basic project layout and corresponding functionalities.

```
.
├── LICENSE
├── README.md
├── ansible.cfg
├── hosts.ini
├── playbook.yml
├── requirements.yml              -- Dependencies
├── roles                         -- User-Defined Roles Directory
│   ├── account                   -- User Account Management
│   ├── certbot                   -- Certbot Functionality
│   ├── jane                      -- Project Deployment
│   └── packages                  -- Software Dependencies
└── vars
    ├── env.yml                   -- Project Environmental Variables
    └── user.yml                  -- User Account Credentials
```  

## Get started

### Access the project
clone project to your local environment.

```
$ git clone git@github.com:kvko/infra-ansible.git
```

### Install roles
Ansible Galaxy refers to the Galaxy website, a free site for finding, downloading, and sharing community developed roles.


To install developed roles in Galaxy:

```
$ cd PROJECT_DIR
$ ansible-galaxy install -r requirements.yml
```

### Run the project
To edit the credential file inside `vars` directory, using the following command.

```
$ ansible-vault edit vars/user.yml
```

Run the playbook to provision the server. You will be ask to enter vault password before proceeding.

```
$ ansible-playbook playbook.yml --ask-vault-pass
```

## References

[ansible_devops]: https://www.goodreads.com/book/show/27111284-ansible-for-devops
[ansible_docs]: https://docs.ansible.com/ansible/latest/index.html

- [Ansible for DevOps by Jeff Geerling (2nd Edition)][ansible_devops]
- [Ansible Documentation][ansible_docs]

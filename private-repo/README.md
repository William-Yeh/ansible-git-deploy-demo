Example #1: public git repo
===

## Preparation

Install roles from Ansible Galaxy:

```
$ ansible-galaxy install -f  -r requirements.yml
```

Modify `project_git_repo` in `playbook.yml`:

```
$ vi playbook.yml
```



## Usage: using Vagrant

Start and provision the virtual machine instance:

```
$ vagrant up
```

Ssh into the virtual machine instance to verify:

```
$ vagrant ssh
```



## Usage: using remote host

Step 1 - edit inventory file:

```
$ vi hosts
```


Step 2 - run ansible-playbook:

```
$ ansible-playbook  \
      --private-key $HOME/.ssh/MY-PRIVATE-KEY.pem  \
      -i hosts  \
      playbook.yml
```


Finally, ssh into the instance to verify!

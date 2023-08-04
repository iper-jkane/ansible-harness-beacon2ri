## An ansible artifact + role to install 
##  the Beacon Reference Implementation v2

tl;dr

```

# Install ansible into virtualenv 
python3 -mvenv --copies ~/pyvirts/ansible
source ~/pyvirts/ansible/bin/activate
pip install -U pip
pip install ansible==5.7.0

# conigure target servers + ansible
## TODO.

# clone the harness + role (as submodule)
git clone --recurse-submodules https://github.com/iper-jkane/ansible-harness-beacon2ri
cd ansible-harness-beacon2ri

# point it at an opensuse/SLES host
ansible-playbook -i hosts b2ri-setup.yml --limit <hostname> 

# list tags + tasks
ansible-playbook -i hosts b2ri-setup.yml --list-tags
ansible-playbook -i hosts b2ri-setup.yml --list-tasks
```

###
Tested against:

  - OpenSUSE: v15.5


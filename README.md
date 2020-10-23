# ansible-role-default-packages

# This Role can be used for install the default packages when you need or when you are changing computer

```
make venv && make default-packages
```

# you can change the packages editing list packages in vars file

```
system_packages:
  - bat
  - pwgen
  - redis-tools
  - hydra
  - jq
  - npm
  - gcc
  - make

network_packages:
  - ngrep
  - net-tools
  - nmap
  - iperf

editor_packages:
  - vim
  - atom
  - gedit

```

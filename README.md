# Openshift Login - Identity Provider combolist


* For apply, edit the file master-config.yaml:

```
vim /etc/origin/master/master-config.yaml
```


* Add the line providerSelection in the file master-config.yaml in all master servers

```
oauthConfig:
  templates:
    providerSelection: templates/select-provider-template.html
```


* Restart all master servers to apply

```
ansible -i <inventory> masters -m shell -a "reboot"
```

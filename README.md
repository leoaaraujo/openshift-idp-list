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

<img width="595" alt="01" src="https://user-images.githubusercontent.com/42226866/58378656-c5e82900-7f6d-11e9-8222-6d634e27c63c.png">

<img width="602" alt="02" src="https://user-images.githubusercontent.com/42226866/58378655-c5e82900-7f6d-11e9-9ff3-23aae25d4306.png">

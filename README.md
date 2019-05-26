# Openshift Login - Identity Provider combolist


* Para aplicar, edite o arquivo master-config.yaml:

...
vim /etc/origin/master/master-config.yaml
...


* Add a linha providerSelection no arquivo master-config.yaml em todos os masters

...
oauthConfig:
  templates:
    providerSelection: templates/select-provider-template.html
...


* Reinicie todos os masters para aplicar

...
ansible -i <inventory> masters -m shell -a "reboot"
...

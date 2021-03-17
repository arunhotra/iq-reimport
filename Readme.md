## ReImporting BIG-IP's using the BIG-IQ REST API.

### Roles used

- manage-secret - to manage secrets bigiq and bigip passwords - create your own secrets.yml with these two variables (vault_bigip_password and vault_bigiq_password)
- obtain-bigips - to get a list of BIG-IPs to reimport (just using csv file here - but it can be obtained in any manner)
- import-bigips - for reimporting BIG-IPs



[BIG-IQ device discovery ansible module](https://clouddocs.f5.com/products/orchestration/ansible/devel/modules/bigiq_device_discovery_module.html#bigiq-device-discovery-module)

### To encrypt your secrets file 

ansible-vault encrypt filename

## This code can be run with cli or awx

To run with cli - ansible-playbook playbooks/bigip-import.yml --ask-vault-pass
To run it with tower/awx, fork the repo and make necessary changes. Then create credentials, scm project and inventory (BIG-IQ). Then create your template.


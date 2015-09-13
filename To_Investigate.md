## There appear to be an errors in this repo.

1. Why is there a /splunk_creds folder under playbooks/splunk_creds?
1. Several cred files are instantiated under playbooks/splunk_creds/splunk_creds
1. Why are the binaries / splunk packages stored in multiple places throughout the repo ?
1. Why is the package file included as a var within search_heads.yml and universal_forwarders.yml but not in common.yml or indexers.yml ?

## To Do

1. OK: Correct repo structure issues
1. Apply consistent standard for placement of binaries and use of vars
1. Encrypt sensitive files with Ansible Vault
1. Configure / make possible true splunk distributed deployment
  * deploy server
  * correct initial ~etc/apps/{corp}_deploymentclient.conf << dbl-check app-name
  purpose is to tell new UFs where the deploy master is. Once contacted, the deploy master
  will overwrite with correct core config
1. add Azure IaaS support
1. add tags to allow consolidation of functions onto fewer servers ( e.g. license and deploy on same server )
1. add support for OpenSUSE and SLES 11 and 12
1. add prompts to ensure type of deployment is specified ( simple, distributed deployment, clustered indexers, etc...)

----
_david kadow_

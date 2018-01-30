# Kubernetes LDAP Authentication

## Environment Variables Required

|Key|Description/Example of Value|
|--|--|
|AUTHORIZATION_HEADER|Token for accessing Kubernetes dashboard (used for all users). Get this from kubectl (see https://github.com/kubernetes/dashboard/wiki/Access-control)|
|AUTH_NAME|Arbitrary name, no spaces. What users see when they are asked for credentials|
|LDAP_BIND_DN|LDAP bind user. Needs to be full DN (including the uid=xxxx,ou=yyyy,dc=zzz)|
|LDAP_BIND_PASSWORD|The LDAP bind password|
|LDAP_REQUIRED_GROUP|The full DN of an LDAP group that someone needs to be a member of to access the dashboard|
|LDAP_URL|LDAP URI. Example: ldaps://ldap.jumpcloud.com:636/ou=Users,o=123456789,dc=jumpcloud,dc=com|
|PROXY_URL|https://kubernetes-dashboard.kube-system:443/ - probably this unless you've changed it to something else|
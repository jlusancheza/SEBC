```
[libdefaults] 
default_realm = EC2.INTERNAL
dns_lookup_kdc = true
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = rc4-hmac
default_tkt_enctypes = rc4-hmac
permitted_enctypes = rc4-hmac
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
EC2.INTERNAL = {
kdc = ip-10-0-3-96.ec2.internal:88
admin_server = ip-10-0-3-96.ec2.internal:749
}
[domain_realm]

```
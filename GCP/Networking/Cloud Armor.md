# Google Cloud Armor

The [Google Cloud Armor](https://cloud.google.com/armor) Protects your services against denial of service and web attacks

* Works with Global HTTP(S) Load Balancer
* IP-based Access Control - Permit or block your incoming traffic based on IP addresses or ranges using allow lists and deny lists.
* Stackdriver logging - Get visibility into the policy and rule matched and the action taken by the rule for each incoming request.
* Attach the policy to a Load Balancer backend in the Cloud Armor settings

## Limitations

* Each project is limited to a max of 200 security rules
* Each project is limited to a max of 10 cloud armor security policies
* Each rule is limited to a max of 5 IP addresses or IP address ranges
* Limit of 20,000 RPS per project across all backends

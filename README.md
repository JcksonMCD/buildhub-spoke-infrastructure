# buildhub-spoke-infrastructure
Next steps.
Build hub and spoke infrastructure.
Have a "central" virtual network, that holds a database, an api-gateway and 2 lambdas (thing1 and thing2)
Include a security group that allows ingress to these resources only from the spokes.
The spokes should include 2 vms (make sure its the cheapest available) and an internet gateway to give the vm internet access.
A route table set up to point all IP's to the internet gateway, apart from the database, api-gateway and lambdas in the central virtual network.
A virtual network with peering to the central network to allow access to the infrastructure there.
A s3 bucket
A load balancer that has a backend pool of the 2 vms.
Include a security group that allows ingress only from the answer office IP.
The spokes should be spun up depending on a input list. So a dynamic amount of spokes depending on how many items in the list.
The list will be a list of names, ["Trust1", "Trust2"]
Make sure everything is tagged. https://answerconsulting.jira.com/wiki/spaces/ARCH/pages/3204907011/Tagging+Policy a gist of what tags you should be including.
All work PR to me and we can go over it.


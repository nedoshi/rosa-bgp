
* VM with primary CUDN
    * CUDN VM A/B traffic to Internet
    * Same VPC to CUDN A/B VM
    * External VPC to transit gateway to CUDN VM A/B
    * CUDN VM A/B to same VPC
    * CUDN VM A/B to transit gateway to external VPC
    * CUDN VM A/B to kapi/dns
    * CUDN VM A/B to host API service
    * CUDN A VM to CUDN A VM (on the same/diff node)
    * CUDN A VM to CUDN B VM (on the same/diff node)
    * same host to CUDN A/B VM (what does this mean?)
    * Diff host to CUDN A/B VM (what does this mean?)
* ClusterIP Service with same L2 network
    * VM to clusterIP(internalTrafficPolicy=Cluster) with same/diff node
    * VM to clusterIP(internalTrafficPolicy=Local) with same/diff node
    * Expose through ClusterIP service?
* NodePort Service with same L2 network
    * VM to NodePort(ETP=Cluster) with same/diff node
    * VM to NodePort(ETP=Local) with same node
    * VM to NodePort(ETP=Local) with diff node (destionation with two backend pods/VMs, one is same as source VM, one is different)
    * VM to NodePort(ETP=Local) with diff node (the source VM is different from any destinaton endpoints nodes)
    * Expose through NodePort service?
* NodePort service with different L2 network
    * VM to NodePort(ETP=Cluster) with same/diff node
    * VM to NodePort(ETP=Local) with same node
    * VM to NodePort(ETP=Local) with diff node (destionation with two backend pods/VMs, one is same as source VM, one is different)
    * VM to NodePort(ETP=Local) with diff node (the source VM is different from any destinaton endpoints nodes)

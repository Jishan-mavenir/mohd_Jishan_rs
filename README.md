DaemonSets should be used when a single copy of your application must run on all or a subset of the nodes in the cluster that means when each node same application 
Maintaining a highly available and scalable Docker registry in Kubernetes is an example for DaemonSet. Ensure your Docker registry always has two replicas running in a cluster-ready state.

Collecting logs from Nodes
Similarly, collecting the contents of Node-level logs (such as Kubelet and kernel logs) helps you audit your environments and troubleshoot problems. Deploying your logging service as a DaemonSet ensures all your Nodes will be included.

Backing up Node data 
Backups are another good candidate for DaemonSets. Using a DaemonSet ensures all your Nodes will be included in your backups without making you scale or reconfigure your backup service when Nodes change. If some Nodes don’t need backups, you can customize your DaemonSet so that only relevant Nodes are covered.

ReplicaSets should be used when your application is completely decoupled from the node and you can run multiple copies on a given node without special consideration. DaemonSets should be used when a single copy of your application must run on all or a subset of the nodes in the cluste.

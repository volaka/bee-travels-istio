# Complete the IBM Cloud set-up for Kubernetes and Istio

1. [Install the IBM Cloud CLI.](https://cloud.ibm.com/docs/cli?topic=cli-getting-started#idt-prereq)

   ```
   curl -fsSL https://clis.cloud.ibm.com/install/linux | sh
   ibmcloud plugin install kubernetes-service

   ```

2. Install kubectl cli

   ```
   curl --progress-bar -LO \
     https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
   ```

3. [Provision a new Kubernetes cluster.](https://istio-workshop.mybluemix.net/) Follow the steps to create a standard classic cluster.

   > NOTE: Request the key from organizator to acquire your pre-provisioned cluster.

4. After Istio has finished installing, install the [`istioctl` CLI](https://istio.io/latest/docs/reference/commands/istioctl/) by running the following:

   ```text
   export ISTIO_VERSION=1.7.3
   curl -L https://istio.io/downloadIstio | sh -
   chmod +x istio-1.7.3/bin/istioctl
   mv istio-1.7.3/bin/istioctl /usr/local/bin/

   ```

5. When your cluster has been created, navigate to the **Add-ons** panel on the left side of your cluster console. Click **Install** for the Managed Istio Add-on.  ![](.gitbook/assets/image%20%289%29.png)
6. [Customize your Istio installation](https://cloud.ibm.com/docs/containers?topic=containers-istio#customize) by following steps 1 through 4 to enable monitoring and increase trace sampling to 100.

   > Your configmap should look like this:   
   > ![](.gitbook/assets/image%20%2818%29.png)


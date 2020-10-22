# Troubleshooting

* Installing Artillery globally as root fails with permission error
  * As suggested [here](https://github.com/artilleryio/artillery/issues/714), try installing Artillery by running `npm install -g artillery --allow-root --unsafe-perm=true`
* Can I check if I have any issues with my Istio configuration?
  * The `istioctl analyze` command can detect possible issues within your cluster. You can also run the command against one or multiple configuration files to analyze the effect of applying them to your cluster. For example: `istioctl analyze istio/ex-virtualservice.yaml`
  * Kiali also has an **Istio Config** panel on the left side of the dashboard that will any warnings or errors in your mesh configuration.
* I'm running a load test with Artillery but only the `bee-ui` service is receiving traffic on Grafana.
  * Check to see that the `target` value in `artillery_load/artillery.yaml` does not have an extra `/` at the end of the address. \(ex: "[http://169.62.94.60](http://169.62.94.60)"\)
* I'm getting a lot of 500 Internal Service Errors when generating traffic with Artillery or in the browser.
  * Your deployments' resource limits may be being reached. Try running `watch -n1 kubectl top po` which displays the resource metrics for each pod updated every second. While this is running, generate traffic to the application to see if any of the pods are exceeding the resource limits set in their respective deployment files. 


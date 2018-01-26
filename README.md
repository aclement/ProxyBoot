# ProxyBoot
A simple boot app able to stand in for a CF deployed app and proxy to other places (using ssh)

There isn't much to this app. Basically it is deployed to PCF and pretends to be an app but
requests that are made to it (once appropriate tunnels have been setup) are routed elsewhere,
usually to a process on the developers local machine.  The aim is that this app is built and
then by using the `cfproxy` script to fill in some parameters, a customized `manifest.yml` is
generated based on the `manifest.yml.template` and that is used to push this app to CF.

ProxyBoot can stand in for any app, it is the yml customization that tailors it to stand in
for a specific app.

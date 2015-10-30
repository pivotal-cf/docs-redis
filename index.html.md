---
title: Redis for Pivotal Cloud Foundry
---

This is documentation for the [Redis service for Pivotal Cloud Foundry](https://network.pivotal.io/products/p-redis).

## Product snapshot

<dl>
<dt>Current Redis for PCF Details</dt>
<dd><strong>Version</strong>: 1.4.10 </dd>
<dd><strong>Release Date</strong>: 16th October 2015</dd>
<dd><strong>Software component version</strong>: Redis OSS 3.0.4</dd>
<dd><strong>Compatible Ops Manager Version(s)</strong>: 1.6.x, 1.5.x</dd>
<dd><strong>Compatible Elastic Runtime Version(s)</strong>: 1.6.x, 1.5.x</dd>
<dd><strong>vSphere support?</strong> Yes</dd>
<dd><strong>AWS support?</strong> Yes</dd>
<dd><strong>OpenStack support?</strong> Yes</dd>
</dl>

## Upgrading to the Latest Version

Consider the following compatibility information before upgrading Redis for Pivotal Cloud Foundry.

<p class="note"><strong>Note</strong>: Before you upgrade to Ops Manager 1.4.x, you must first upgrade Redis for PCF to any 1.4.x version prior to 1.4.4. This allows Redis for PCF upgrades after you install OpsManager 1.4.x. </p>

For more information, refer to the full [Product Version Matrix](../compatibility-matrix.pdf).

<table border="1" class="nice">
<tr>
  <th>Ops Manager Version</th>
  <th>Supported Upgrades from Imported Redis Installation</th>
</tr>
<tr>
  <th>1.3.x</th>
  <td><ul>
      <li>From 1.3.2 to 1.4.0, 1.4.1, 1.4.2</li>
      <li>From 1.4.0 to 1.4.1, 1.4.2, 1.4.3</li>
      <li>From 1.4.1 to 1.4.2, 1.4.3</li>
    </ul>
  </td>
</tr>
<tr>
  <th>1.6.x, 1.5.x and 1.4.x</th>
  <td><ul>
      <li>From 1.4.0 to 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.1 to 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.2 to 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.3 to 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.4 to 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.5 to 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.6 to 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.7 to 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.8 to 1.4.9, 1.4.10</li>
      <li>From 1.4.9 to 1.4.10</li>
    </ul>
  </td>
</tr>
</table>

## Install via Pivotal Operations Manager

To install Redis for PCF, follow the procedure for installing Pivotal Ops Manager tiles:

1. Download the product file from [Pivotal Network](https://network.pivotal.io/).
1. Upload the product file to your Ops Manager installation.
1. Click **Add** next to the uploaded product description in the Available Products view to add this product to your staging area.
1. Click the newly added tile to review any configurable options.
1. Click **Apply Changes** to install the service.

## Available Plans

There are two available plans:

<table border="1" class="nice">
<tr>
<th><strong>Plan Name</strong></th>
<th><strong>Suitable for</strong></th>
<th><strong>Tenancy Model per Instance</strong></th>
<th><strong>Highly Available</strong></th>
<th><strong>Backup Functionality</strong></th>
</tr>

<tr>
<td><b>Shared-VM</b></td>
<td>Development and testing workloads</td>
<td>Shared VM</td>
<td>No</td>
<td>No</td>
</tr>

<tr>
<td><b>Dedicated-VM</b></td>
<td>Production workloads</td>
<td>Dedicated VM</td>
<td>No</td>
<td>No</td>
</tr>

</table>

## Provisioning and Binding via Cloud Foundry

Once you have installed the product, it automatically registers itself with your Elastic Runtime. At this point, the product is available to your application developers, either in the Marketplace in the web based console, or via `cf marketplace`. They can add, provision, and bind the service to their applications like any other CF service:

```
$ cf create-service p-redis shared-vm redis
$ cf bind-service my-application redis
$ cf restart my-application
```

## Security
The following ports & ranges are used in this service:

* Destination port 80 access to the service broker from the cloud controllers
* Destination port 6379 access to all dedicated nodes from the DEA network(s)
* Destination ports 32768 to 61000 on the service broker from the DEA network(s). This is only required for the shared service plan.

## Example Application

To help your application developers get started with Redis for PCF, we have provided an example application, which can be [downloaded here](https://github.com/pivotal-cf/cf-redis-example-app/archive/master.zip).

## Feedback

Please provide any bugs, feature requests, or questions to [the Pivotal Cloud Foundry Feedback list](mailto:pivotal-cf-feedback@pivotal.io).

## Further Reading

* [Official Redis Documentation](http://redis.io/documentation)

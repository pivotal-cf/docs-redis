---
title: Redis for Pivotal Cloud Foundry
---

Release notes for [Redis for Pivotal Cloud Foundry](https://network.pivotal.io/products/p-redis)

### 1.4.10
**Release Date: 16th October 2015**

Features included in this release:

* Certified with PCF Suite 1.6
* Updated stemcell to 3100
* Updated Redis to 3.0.4

### 1.4.9
**Release Date: 7th October 2015**

Features included in this release:

* Update stemcell to 3094 to address [USN-2765-1](http://www.ubuntu.com/usn/usn-2765-1/)

Known issues:

* Note one important known issue with the 1.5.6 patch for Openstack deployments. BOSH stemcell v3094, which this version of Elastic Runtime references, has a limitation affecting Openstack users only:
  * Elastic Runtime 1.5.6 on Openstack does not work with S3/Swift blobstores.
  * Elastic Runtime 1.5.6 on Openstack users must configure their object storage to use the internal blobstore option.
  * vSphere, AWS and vCloud users are not affected.

### 1.4.8
**Release Date: 2nd September 2015**

Features included in this release:

* Updated stemcell to 3062

### 1.4.7
**Release Date: 29th July 2015**

Features included in this release:

* Updated stemcell to 3026 to resolve CVE-2015-3290

### 1.4.6
**Release Date: 6th July 2015**

Features included in this release:

* Support for OpsManager 1.5.x or 1.4.x
* Support for Elastic Runtime 1.5.x or 1.4.x
* Support for HTTPS-only environments
* Support for vSphere or AWS Deployments
* Requires stemcell 2989
* Fixes a bug where credentials are double escaped after upgrading from Redis 1.3.2 and then re-binding existing instances.

### 1.4.5
**Release Date: 15th June 2015**

Features included in this release:

* Latest version of Redis 2.8.21 to resolve the Lua sandbox exploit
* Migration path added from Redis for PCF 1.3.2

Known issues:

* Upgrading from Redis 1.3.2 to this version or prior versions and then re-binding an existing instance can cause the credentials to be double escaped. New instances or existing instances without a re-bind are not impacted.
* On AWS, this version supports deployments in the US-East region. Multi-region support is coming in a future release.
* The experimental HTTPS-only feature in Elastic Runtime 1.5 may cause issues with this version of the product. Full support for HTTPS-only traffic is coming in a future release.

<p class="note"><strong>Note</strong>: BOSH Stemcell 2865.1 is required for installation on Ops Manager 1.5.x and above.</p>

### 1.4.4
**Release Date: 14th May 2015**

Features included in this release:

* Support for OpsManager 1.4.0 or greater
* Support for vSphere or AWS deployments

### 1.4.3
**Release Date: 23rd March 2015**

Features included in this release:

* Updated stemcell to 2889 to resolve [these OpenSSL CVE alerts](http://pivotal.io/security/usn-2537-1)

### 1.4.2
**Release Date: 30th January 2015**

Features included in this release:

* Updated stemcell to 2824 to resolve [CVE-2015-0235 Ghost](http://www.pivotal.io/security/cve-2015-0235)

### 1.4.1
**Release Date: 16th January 2015**

Features included in this release:

* Latest version of Redis 2.8.19
* Latest version of Nginx 1.7.9

### 1.4.0
**Release Date: 15th December 2014**

Features included in this release:

* New service plan called `dedicated-vm`
  * Pre-provisions a pool of VMs upon deploying the tile
  * An instance of this plan provides a single dedicated VM, with a single Redis process
  * [See more details here](http://docs.pivotal.io/redis/dedicated-vm.html)
* Latest version of Redis 2.8.18
* `development` service plan renamed to `shared-vm`

### 1.3.2
**Release Date: 6th October 2014**

Features included in this release:

* General Availability release
* `development` service plan, providing a redis process on a shared-vm
  * Suitable for development and test workloads

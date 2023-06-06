# Redis for VMware Tanzu Application Service Docs

This repo contains the Redis for VMware Tanzu Application Service documentation.

In this README:

- [Branches in this Content Repo](#branches-in-this-content-repo)
- [Releasing a New Minor Version](#releasing-a-new-minor-version)
- [Partials](#partials)
- [Contributing to Documentation](#contributing-to-documentation)
- [Publishing Docs](#publishing-docs)
- [Troubleshooting Markdown](#troubleshooting-markdown)
- [Style Guide](#style-guide)

## Branches in this Content Repo

### main - Use for next unreleased version

All documentation for the next unreleased version of Redis is in `main`.

Always make changes you want carried forward in the main branch. This includes:

* Unreleased features
* Doc bug fixes
* Doc reorganization or enhancement

Staging link: https://docs-staging.vmware.com/en/draft/Redis-for-VMware-Tanzu-Application-Service/3.2/redis-tanzu-application-service/GUID-index.html

### Live Branches In Production (Public)

* **3.2**: Live docs at staging (https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.2/redis-tanzu-application-service/GUID-index.html) and production (https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.2/redis-tanzu-application-service/GUID-index.html)
* **3.1**: Live docs at staging (https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.1/redis-tanzu-application-service/GUID-index.html) and production (https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.1/redis-tanzu-application-service/GUID-index.html)
* **3.0**: Live docs at staging (https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.0/redis-tanzu-application-service/GUID-index.html) and production (https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.0/redis-tanzu-application-service/GUID-index.html)
* **2.4**: Live docs at staging (https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.4/redis-tanzu-application-service/GUID-index.html)and production (https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.4/redis-tanzu-application-service/GUID-index.html)
* **2.3**: Live docs at staging (https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.3/redis-tanzu-application-service/GUID-index.html) and production (https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.3/redis-tanzu-application-service/GUID-index.html)
* **2.2**: This branch is no longer in use because this version is EOGS. PDF available at https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.2/redis-for-tas-2-2.pdf
* **2.1**: This branch is no longer in use because this version is EOGS. PDF available at https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.1/redis-for-tas-2-1.pdf
* **2.0**: This branch is no longer in use because this version is EOGS. PDF available at https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.0/redis-for-tas-2-0.pdf
* **1.14**: This branch is no longer in use because this version is EOGS. PDF available at https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/1.14/redis-for-tas-1-14.pdf
* **1.13**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.13.pdf.
* **1.12**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.12.pdf.
* **1.11**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.11.pdf.
* **1.10**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.10.pdf.
* **1.9**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.9.pdf.
* **1.8**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.8.pdf.
* **1.7**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.7.pdf.
* **1.6**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.6.pdf.
* **1.5**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.5.pdf.
* **1.5**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.5.pdf.
* **1.4**: This branch is no longer in use because the docs are no longer live. PDF available at https://docs.pivotal.io/archives/redis-1.4.pdf.

### Cherry picking to and from main

1. Always cherry-pick any changes to live branches into **main** if you want those changes carried forward.

2. If necessary, immediately cherry-pick/copy changes from **main** that you want to push immediately to production into the appropriate live branch above.

## Releasing a New Minor Version

Because **main** is the latest and greatest documentation, the process would be to cut a **x.x** branch
for the version that **main** was targeting during that time.

After this point, **main** will then be the target for the next version of this product.

## Partials

Cross-product partials for **Redis for VMware Tanzu Application Service** are single sourced from the [Services Partials](https://github.com/pivotal-cf/docs-partials) repository.

Previously, these partials were sourced from the v018.x branch of the [On Demand Service Broker SDK](https://github.com/pivotal-cf/docs-on-demand-service-broker/tree/v0.18.x) content repository.

## Contributing to Documentation

If there is some documentation to add for an unreleased patch version of Redis for VMware Tanzu Application Platform then create a branch off of the **live** branch
you intend to modify and create a pull request against that branch.
After the version that change is targeting is released, the pull request can be merged and will be live
the next time a documentation deployment occurs.

If the documentation is meant to be target several released versions,
then you will need to:
+ create a pull request for each individual minor version
+ or ask the technical writer to cherry-pick to particular branches/versions.

For instructions on how to create a pull request on a branch and instructions on how to create a
pull request using a fork, see
[Creating a PR](https://docs-wiki.sc2-04-pcf1-apps.oc.vmware.com/wiki/external/create-pr.html)
in the documentation team wiki.


## Publishing Docs

- [docworks](https://docworks.vmware.com/) is the main tool for managing docs used by writers.
- [docsdash](https://docsdash.vmware.com/) is a deployment UI which manages the promotion from
staging to pre-prod to production. The process below describes how to upload our docs to staging,
replacing the publication with the same version.

### Prepare Markdown Files
- Markdown files live in this repo.
- Images should live in an `images` directory at the same level and linked with a relative link.
- Each page requires an entry in [config/toc.md](config/toc.md) for the table of contents.
- Variables live in [config/template_variables.yml](config/template_variables.yml).

### In Docsdash

1. Wait about 1 minute for processing to complete after uploading.
2. Go to https://docsdash.vmware.com/deployment-stage

   There should be an entry with a blue link which says `Documentation` and points to staging.

### Promoting to Pre-Prod and Prod

**Prerequisite** Needs additional privileges - reach out to a manager on the docs team [#tanzu-docs](https://vmware.slack.com/archives/C055V2M0H) or ask a writer to do this step for you.

1. Go to Staging publications in docsdash
  https://docsdash.vmware.com/deployment-stage

2. Select a publication (make sure it's the latest version)

3. Click "Deploy selected to Pre-Prod" and wait for the pop to turn green (refresh if necessary after about 10s)

4. Go to Pre-Prod list
  https://docsdash.vmware.com/deployment-pre-prod

5. Select a publication

6. Click "Sign off for Release"

7. Wait for your username to show up in the "Signed off by" column

8. Select the publication again

9. Click "Deploy selected to Prod"


## Troubleshooting Markdown

| Problem | List displays as a paragraph |
|---------|-----------|
| Symptom:| Bulleted or numbered lists look fine on GitHub but display as a single paragraph in HTML.|
| Solution: | Add a blank line after the stem sentence and before the first item in the list.|

| Problem | List numbering is broken: every item is `1.` |
|---------|-----------|
| Symptom:| Each numbered item in a list is a `1.` instead of `1.`, `2.`, `3.`, etc|
| Solution: | Try removing any blank newlines within each step.|

| Problem | Code boxes not showing |
|---------|-----------|
| Symptom:| VMware publishing system doesn't accept code tags after the three back ticks.|
| Solution: | Make sure you're not using `shell` or `bash` or `console` or `yaml` after back ticks.|


## Style Guide

Use this section to specify spelling of special words for Redis for VMware Tanzu Application Service:

+ on-demand plan
+ shared-VM plan

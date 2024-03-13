# Redis for VMware Tanzu Application Service Docs

This repo contains the Redis for VMware Tanzu Application Service documentation.

In this README:

- [Redis for VMware Tanzu Application Service Docs](#redis-for-vmware-tanzu-application-service-docs)
  - [Branches](#branches)
    - [Master - Use for next unreleased version](#master---use-for-next-unreleased-version)
    - [Released branches](#released-branches)
    - [Cherry picking to and from MASTER](#cherry-picking-to-and-from-master)
  - [Releasing a new minor version](#releasing-a-new-minor-version)
  - [Partials](#partials)
  - [Contributing to documentation](#contributing-to-documentation)
  - [Publishing docs](#publishing-docs)
    - [Prepare Markdown files](#prepare-markdown-files)
    - [In Docsdash](#in-docsdash)
    - [Promoting to pre-prod and prod](#promoting-to-pre-prod-and-prod)
  - [Troubleshooting Markdown](#troubleshooting-markdown)
  - [Style guide](#style-guide)

## Branches

### Master - Use for next unreleased version

All documentation for the next unreleased version of Redis is in `master`.

Always make changes you want carried forward in the master branch. This includes:

* Unreleased features
* Doc bug fixes
* Doc reorganization or enhancement

[Staging link for main](https://docs-staging.vmware.com/en/draft/Redis-for-VMware-Tanzu-Application-Service/3.5/redis-tanzu-application-service/GUID-index.html)

### Released branches

* [3.4 staging](https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.4/redis-tanzu-application-service/GUID-index.html) and [3.4 production](https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.4/redis-tanzu-application-service/GUID-index.html)
* [3.3 staging](https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.3/redis-tanzu-application-service/GUID-index.html) and [3.3 production](https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.3/redis-tanzu-application-service/GUID-index.html)
* [3.2 staging](https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.2/redis-tanzu-application-service/GUID-index.html) and [3.2 production](https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.2/redis-tanzu-application-service/GUID-index.html)
* [3.1 staging](https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.1/redis-tanzu-application-service/GUID-index.html) and [3.1 production](https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.1/redis-tanzu-application-service/GUID-index.html)
* [3.0 staging](https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.0/redis-tanzu-application-service/GUID-index.html) and [3.0 production](https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/3.0/redis-tanzu-application-service/GUID-index.html)
* [2.4 staging](https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.4/redis-tanzu-application-service/GUID-index.html) and [2.4 production](https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.4/redis-tanzu-application-service/GUID-index.html)
* [2.3 staging](https://docs-staging.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.3/redis-tanzu-application-service/GUID-index.html) and [2.3 production](https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.3/redis-tanzu-application-service/GUID-index.html)
* **2.2**: This branch is no longer in use because this version is EOGS. PDF available at https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.2/redis-for-tas-2-2.pdf
* **2.1**: This branch is no longer in use because this version is EOGS. PDF available at https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.1/redis-for-tas-2-1.pdf
* **2.0**: This branch is no longer in use because this version is EOGS. PDF available at https://docs.vmware.com/en/Redis-for-VMware-Tanzu-Application-Service/2.0/redis-for-tas-2-0.pdf
* **1.14 and earlier**: These branches are no longer in use. They are EOGS and removed from the docs.VMware site.

### Cherry picking to and from MASTER

1. Always cherry-pick any changes to live branches into **master** if you want those changes carried forward.

2. If necessary, immediately cherry-pick/copy changes from **master** that you want to push immediately to production into the appropriate live branch above.

## Releasing a new minor version

Because **master** is the latest and greatest documentation, the process would be to cut a **x.x** branch
for the version that **master** was targeting during that time.

After this point, **master** will then be the target for the next version of this product.

## Partials

Cross-product partials for **Redis for VMware Tanzu Application Service** are single sourced from the [Services Partials](https://github.com/pivotal-cf/docs-partials) repository.

## Contributing to documentation

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


## Publishing docs

- [docworks](https://docworks.vmware.com/) is the main tool for managing docs used by writers.
- [docsdash](https://docsdash.vmware.com/) is a deployment UI which manages the promotion from
staging to pre-prod to production. The process below describes how to upload our docs to staging,
replacing the publication with the same version.

### Prepare Markdown files

- Markdown files live in this repo.
- Images should live in an `images` directory at the same level and linked with a relative link.
- Each page requires an entry in [config/toc.md](config/toc.md) for the table of contents.
- Variables live in [config/template_variables.yml](config/template_variables.yml).

### In Docsdash

1. Wait about 1 minute for processing to complete after uploading.
2. Go to https://docsdash.vmware.com/deployment-stage

   There should be an entry with a blue link which says `Documentation` and points to staging.

### Promoting to pre-prod and prod

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


## Style guide

Use this section to specify spelling of special words for Redis for VMware Tanzu Application Service:

+ on-demand plan
+ shared-VM plan

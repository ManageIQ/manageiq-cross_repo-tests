# ManageIQ cross-repository testing framework tests

This repo is used to execute cross-repository tests for the ManageIQ project.

## Usage

In order to use this repo, create a pull request modifying the .travis.yml file
and setting the `TEST_REPO` and `REPOS` environment variables as needed.

For more information about the variables or more examples, refer to the
[manageiq-cross_repo gem](https://github.com/ManageIQ/manageiq-cross_repo/blob/master/README.md).

## Examples

#### Testing a single repo in the context of ManageIQ PR 12345

```diff
@@ -14,6 +14,6 @@ matrix:
   fast_finish: true
 env:
   global:
-  - REPOS=
+  - REPOS=manageiq#12345
   matrix:
-  - TEST_REPO=
+  - TEST_REPO=manageiq-ui-classic
```

#### Testing multiple repos in the context of ManageIQ PR 12345

```diff
@@ -14,6 +14,7 @@ matrix:
   fast_finish: true
 env:
   global:
-  - REPOS=
+  - REPOS=manageiq#12345
   matrix:
-  - TEST_REPO=
+  - TEST_REPO=manageiq-ui-classic
+  - TEST_REPO=manageiq-api
```

#### Testing multiple repos in the context of ManageIQ branch "gaprindashvili"

```diff
@@ -14,6 +14,7 @@ matrix:
   fast_finish: true
 env:
   global:
-  - REPOS=
+  - REPOS=manageiq@gaprindashvili
   matrix:
-  - TEST_REPO=
+  - TEST_REPO=manageiq-ui-classic
+  - TEST_REPO=manageiq-api
```

`Same syntax is used for tags`

##### Full List of Providers
    manageiq-providers-amazon
    manageiq-providers-ansible_tower
    manageiq-providers-autosde
    manageiq-providers-azure
    manageiq-providers-azure_stack
    manageiq-providers-foreman
    manageiq-providers-google
    manageiq-providers-ibm_cloud
    manageiq-providers-ibm_terraform
    manageiq-providers-kubernetes
    manageiq-providers-kubevirt
    manageiq-providers-lenovo
    manageiq-providers-nsxt
    manageiq-providers-openshift
    manageiq-providers-openstack
    manageiq-providers-ovirt
    manageiq-providers-redfish
    manageiq-providers-scvmm
    manageiq-providers-vmware

## License

Open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

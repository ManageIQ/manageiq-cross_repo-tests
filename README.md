# ManageIQ cross-repository testing framework tests

This repo is used to execute cross-repository tests for the ManageIQ project.

## Usage

In order to use this repo, create a pull request modifying the .travis.yml file
and setting the `TEST_REPO`, `CORE_REPO`, and `GEM_REPOS` environment variables
as needed.

For more information about the variables or more examples, refer to the
[manageiq-cross_repo gem](https://github.com/ManageIQ/manageiq-cross_repo/blob/master/README.md).

## Examples

#### Testing a single repo in the context of ManageIQ PR 12345

```diff
@@ -11,6 +11,5 @@ matrix:
   fast_finish: true
 env:
   global:
-  - TEST_REPO=
-  - CORE_REPO=
-  - GEM_REPOS=
+  - TEST_REPO=manageiq-ui-classic
+  - CORE_REPO=manageiq@12345
```

#### Testing multiple repos in the context of ManageIQ PR 12345

```diff
@@ -11,6 +11,7 @@ matrix:
   fast_finish: true
 env:
   global:
-  - TEST_REPO=
-  - CORE_REPO=
-  - GEM_REPOS=
+  - CORE_REPO=manageiq@12345
+  matrix:
+  - TEST_REPO=manageiq-ui-classic
+  - TEST_REPO=manageiq-api
```

## License

Open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

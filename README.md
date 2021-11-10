# RevBayes Integration Tests

This repository contains the integration test suite for RevBayes. Individual tests are stored in directories beginning with `test_` and are run automatically by the script `run_integration_tests.sh`. The return status of this script is used to determine whether the tests have passed.

## Website tutorials

The RevBayes website tutorials can also be tested using this script by placing a `test.sh` script in the appropriate tutorial directory on the [RevBayes website repository](https://github.com/revbayes/revbayes.github.io). The RevBayes website is used as a submodule of this repository and is automatically cloned and updated by the `run_integration_tests.sh` script. In order to clone and update it manually, you can use

```
git submodule update --init --recursive
```

This will clone the RevBayes website as a submodule directory. In order to test against a specific commit in the website repository, you should checkout that commit in the submodule.

## Updating the tests

Updating the test output or adding new tests requires both changes to this repository, as well as a change to the main RevBayes repository to update the version of the tests repository used by the main repository. Step-by-step instructions:

 * make changes to the tests
 * add and commit changes to the tests repository (using `git add` and `git commit` from within the `tests` folder)
 * push the changes to the tests repository (using `git push` from within the `tests` folder). This requires no special permission or review.
 * update the tests version used by the main repository (using `git add tests`, `git commit` and `git push` from within the `revbayes` folder)
 * note that the tests version is specific to each branch, so your new/updated tests will only be used by the `development` branch once a PR has been made and merged in the main repository


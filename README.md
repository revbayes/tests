# RevBayes Integration Tests

This repository contains the integration test suite for RevBayes. Individual tests are stored in directories beginning with `test_` and are run automatically by the script `run_integration_tests.sh`. The return status of this script is used to determine whether the tests have passed.

The RevBayes website tutorials can also be tested using this script by placing a `test.sh` script in the appropriate tutorial directory on the [RevBayes website repository](https://github.com/revbayes/revbayes.github.io). The RevBayes website is used as a submodule of this repository and is automatically cloned and updated by the `run_integration_tests.sh` script. In order to clone and update it manually, you can use

```
git submodule update --init --recursive
```

This will clone the RevBayes website as a submodule directory. In order to test against a specific commit in the website repository, you should checkout that commit in the submodule.


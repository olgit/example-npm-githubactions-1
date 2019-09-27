# Black Duck CoPilot npm/Travis CI Example

[![Build Status](https://travis-ci.org/BlackDuckCoPilot/example-npm-travis.svg?branch=master)](https://travis-ci.org/BlackDuckCoPilot/example-npm-travis) [![Black Duck Security Risk](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-npm-travis/branches/test/badge-risk.svg)](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-npm-travis/branches/test)

Shows a working setup for using Black Duck CoPilot to analyze the risk of project dependencies

## Travis CI Setup
The `.travis.yml` file has been modified to upload generated dependency data to CoPilot:

```yaml
after_success:
  - bash <(curl -s https://copilot.blackducksoftware.com/ci/travis/scripts/upload)
```

# Black Duck CoPilot Gradle/GitHub CI Example

[![Actions](https://github.com/BlackDuckCoPilot/example-npm-githubactions/workflows/Java%20CI/badge.svg)](https://github.com/BlackDuckCoPilot/example-npm-githubactions/actions?workflow=Java+CI) [![Black Duck Security Risk](https://copilot-valid.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-npm-githubactions/branches/validation/badge-risk.svg)](https://copilot-valid.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-npm-githubactions/branches/validation)

Shows a working setup for using the Black Duck CoPilot integration to analyze the risk of project dependencies

## GitHub CI/CD Setup

The `.github/workflows/workflow.yml` file has been modified to upload generated dependency data to Black Duck CoPilot:

```yaml
- name: Set up Java (CoPilot)
  uses: actions/setup-java@v1
  with:
    java-version: 1.8
- name: Upload to CoPilot
      run: bash <(curl -s https://copilot-valid.blackducksoftware.com/ci/githubactions/scripts/upload)
```

# Allset action for running automated end-to-end and integration tests against deployed environments.

## Usage
Adding the following to your workflow will allow you to run automated tests against the environment you just deployed to.

```yaml
- name: Smoke tests
  uses: AllsetHQ/action-web-tests@master
  with:
    environment: edge
    package_token: ${{ secrets.PACKAGE_TOKEN }}
    repo_token: ${{ secrets.WEB_TESTS_DEPLOY_KEY }}
```

### Inputs
#### Parameters
|name|description|required|default|
|---|---|---|---|
|`environment`| The environment to run against. E.g. 'edge', or 'production'. |true|-|
|`package_token`| The token used to access private AllsetHQ npm packages. |true|-|
|`repo_token`| The private SSH Deploy Key used to clone the tests repo. |true|-|

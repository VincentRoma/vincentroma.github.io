## How to integrate automated tests using Nock & CircleCI

#### Nock

[Nock](https://github.com/node-nock/nock) is an HTTP mocking and expectations library for Node.js

We use it to mock calls to remote API or to local database.

#### CircleCI

[CircleCI](https://circleci.com/) is a continuous integration tool you can plug directly to Github repositories and it's creating WebHooks to detect new commits, run tests and display results in Github before you merge branches.

#### Exemple

1. Doing some code modifications and pushing it to Github, CircleCI starts running tests.

![Test Circle Ci](http://94.23.63.76/testci.png)

2. Opening a pull request to merge my code, CircleCI shows tests running status on Github.

![Test Running Github](http://94.23.63.76/testruningpr.png)

3. My code is bad, test failed

![Test Fails Github](http://94.23.63.76/testfail.png)

4. Fixing the code and pushing again

![Test Pass Github](http://94.23.63.76/testpass.png)

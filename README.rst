Install CLI
-----------

curl -fLSs https://circle.ci/cli | bash
circleci update
circleci switch

Creating Orbs
-------------
https://circleci.com/docs/2.0/creating-orbs/#section=configuration

circleci namespace create cjw296 github cjw296
circleci orb create cjw296/playground-orb
circleci orb publish python-ci.yaml cjw296/python-ci@dev:current
circleci orb publish promote cjw296/python-ci@dev:current [major|minor|patch]

Existing Orbs
-------------
https://circleci.com/orbs/registry/

Docker Files
------------
https://github.com/circleci-public/circleci-dockerfiles

Setting up a new repo
---------------------

- Make sure carthorse-cjw296 can write to the repo (add as a collaborator!)
  - accept the invite from a carthorse-logged-in-browser
  - https://circleci.com/add-projects/gh/cjw296 - or pick another org
  - Click "Start Building"
- On CircleCI, for the repo, go to Settings -> Checkout SSH Keys:
     - make sure carthorse-cjw296 is the preferred one.
- On CircleCI, for the repo, go to Settings -> Advanced Settings:
     - make sure "Build forked pull requests" is on
- On CircleCI, add PYPI_PASS env var at https://circleci.com/gh/cjw296/<project>/edit#env-vars

# matrix-questionnaire

Student project to do POC for a matrix questionnaire system

Starting August 2017 we will be developing a questionnaire to support matrix evaluation, where areas of questions can be described in rows by columns supporting a scoring system for areas and difficulty.

Such a questionnaire can support our [CoDe Maturity model](http://code-maturity.praqma.com/).

This first content of this repository is just to support some initial ideas and requirements.


Implementation goals are:

* split "what" from "how"
* stateful - be able to save answers and resume questionnaire
_Focus less on visualization and layout in the POC_.


Possible components:

* layout
* web frontend (page)
* scoring system, using accumulated score (support later for individual scoring)
* content to webpage
* Database of some kind for state
* configuration

Questions could very well be like a decision tree, or the model could be based on such so questions are dynamic based on earlier answers.

Support only limited types of question layout, like dropdown or radiobuttons.




Technologies

* deliver using containers
* github, waffle
* Database could be old school relational, or just nosql of some kind
* json and YML for data and configuration


Versioning

A deployed questionnaire have a version, and that make the data gathering from answers based on the version.
Any change in the questions, so they semantically are changed and do not comply with old answers will require major bump in version numbers.

There could be supplied transition rules from one major version to another major version to support moving data forward to newer versions.

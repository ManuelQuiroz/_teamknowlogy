# Demo Intelimetrica

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.7.4.

## Quick start
* Install Node.js. On Linux, install the package manager separately npm
* Once cloned in the repository [_teamknowlogy](https://github.com/ManuelQuiroz/_teamknowlogy), within the project directory, install dependencies:: `npm install`
* After having installed the dependencies run the command `npm start`

## Development environment

Common tasks:

| Task | Command |
|---|---|
| Generate a new component | `ng generate component component-name` |
| Start whole environment and Api Rest served with mocks | `ng serve` |
| Start whole environment and Api Rest development | `ng b --env = dev` |
| Compile project for production, without lifting server. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.| `ng build` |
| Compile project for production, Api Rest productive | `ng build --prod --env = prod -o` |
| Execute unit tests via [Karma](https://karma-runner.github.io)| `ng test` |
| Execute the end-to-end tests via [Protractor](http://www.protractortest.org/).
Before running the tests make sure you are serving the app via `ng serve`.| `ng e2e` |

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).


## Contribution guide

### Remotes
As a rule, `remotes` follow the following nomenclature:
* `origin`: fork of the project in the developer's account
* `upstream`: main repository (https://github.com/ManuelQuiroz/_intelimetrica)

### Content and messages of the commits

####Content

Each commit must refer to a single issue. If there are many changes that affect different pieces,
those changes should be contributed in several commits. If there are several commits on the same element
with successive changes that are correcting themselves, all those commits must come together
(squash) in a single commit before contributing.

Each fix or feature commit must contain the associated sources and tests.

####Messages

The messages should follow the convention established at: https://github.com/conventional-changelog/conventional-changelog

Basically they will follow the format:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```
For example:

```fix (search): filter min / max on amount instead of subsequent balance

Closes # AABB-12345.

The values of min and max filter the list of movements using the value
of its amount and not its subsequent balance.
```
Valid types are:

* ** feat **: New best or feature
* **fix **: Resolution of bugs and incidents
* **docs **: Change of documentation
* **style **: Changes that do not affect the sense of the code (blank spaces,
missing format, period and commas, etc.)
* **refactor **: Code changes that neither solve incidents nor add functionality.
* **test **: Add missing tests or correct existing ones
* **chore **: Changes in construction processes or tools or auxiliary libraries
like .gitignore, .jshint, generation of documentation, etc.



### Incidents

* Never work on `origin` of the project.
* The `origin \ development` branch will be used to create local branches.
It will keep pace with `upstream \ development`, especially at the moment
to create a branch.
* To work on an issue, a branch is created from `development`.
The recommended nomenclature is `inc- [zip_incidence_code]`.
* The incident is resolved and the changes are committed, as indicated above.
* It becomes `push` from the branch to` origin`;
* ** Before making a Merge Request ** a ** pull is made with rebase ** of
`upstream / development` thus ensuring that commits can enter
no problems in the `development` branch.
* The Merge Request is performed. The title must be descriptive regarding the changes or improvements made. In the body will be provided
the opportune information so that the integrator understands the content better
of the Merge Request and should be structured in the following way, in markdown format:

```
## <Contribution type [will group all of your type]>

**<Operative to which it belongs>: **
* **<Screen or corresponding sub-element [if any]>: **
    * <Detailed description of the change or improvement>. <Related incident link [if any]>. (_Developer: <Developer name> / Integrator: <Person to which the Merge Request is assigned> _)
    * Another change [...]
* ** Other Screen: *
    * Another change [...]
```
For example:

```
## Bugfixes

**Express Accounts:**
* **Pre-register:**
    * Fix beneficiary field validation. It only allows entering alphanumeric characters. Incidence of JIRA [APF-000] (https://adesismx.atlassian.net/browse/APF-000). (_Developer: Manuel Quiroz / Integrator: Juan Pérez_)
    * Another change [...]. Incidence of JIRA [APF-000] (https://adesismx.atlassian.net/browse/APF-000). (_Developer: Manuel Quiroz / Integrator: Juan Pérez_)
* **Edit:**
    * Another change [...]. (_Developer: Manuel Quiroz / Integrator: Juan Pérez_)

## Features

**Core:**
* **DirectiveDirectiveName:**
    * Policy is created for [...]. (_Developer: Manuel Quiroz / Integrator: Juan Pérez_)
* **Service nameService:**
    * Service added that [...]. (_Developer: Manuel Quiroz / Integrator: Juan Pérez_)
```
The developer must ensure that the message is displayed correctly, once written (it is recommended to use a markdown previewer).

The integrator may comment and / or demand rectifications or new elements on the Merge Request. If this is the case, you should work on the Merge request, and **never close it to create another new**, since traceability would be lost.

* If you have to add new commits, doing push to `origin`, the Merge Request
It is updated automatically.
* If you have to redo commits (for example, to adjust commit messages,
squash or split commits), the local history will be overwritten. For
send it to the corresponding branch in `origin` you have to do a push force
(`git push -f`). By doing so, the Merge Request is automatically updated.
* **IMPORTANT**: With each change, keep the Merge Request updated by doing the corresponding pull with rebase of `upstream \ development`.


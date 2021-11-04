# How to contribute

Stooa is the Open Source unconference project, and we are really happy to recieve contributions 🎉. There are many different ways to contribute to Stooa’s development, just find the one that best fits with your skills or concerns, not all of them require coding skills or opening pull requests.

## Contribute to the codebase 

To contribute to Stooa's codebase you should fork the project, make your changes locally and then creating a pull request. If you don't know how to do this process properly don't worry, check this quick tutorials about [forking][how_to_fork] and [pull requests][how_to_pr]. (Everyone has been there at some point 😊 )

If it is **the first time** you contribute to Stooa's codebase you will be asked to sign the [DCO License](CONTRIBUTING.md#dco-license), which is basically that you ensure that code is yours, that you are aware of the license we are using, etc...

### Pull requests 

To contribute to the project you have to firstly carefully read the [**DCO**](CONTRIBUTING.md#DCO-license) section, use the pull request system and format your commits accordingly.

If you intend to [fix a bug](CONTRIBUTING.md#bug-fixing) it's fine to submit a pull request right away but we still recommend to file an [issue][issue_bug] detailing what you're fixing. This is helpful in case we don't accept that specific fix but want to keep track of the issue.

Please, when creating a new **pull request** read our template carefully and don't delete it (it will appear when you start a pull request). This will help you to provide all the information needed to understand your contribution, not only to the core team, but also for other contributors.

If you want to implement or start working in a **new feature**, please open a **question** / **discussion** issue for it. No **pull request** will be accepted without previous chat about the changes, independently if it is a new feature, already planned feature or small quick win.

## Available contributions

* [Bug Report](CONTRIBUTING.md#bug-report)
* [Bug Fixing](CONTRIBUTING.md#bug-fixing)
* [New features](CONTRIBUTING.md#new-features)
* [Third party integration](CONTRIBUTING.md#third-party)
* [Translations](CONTRIBUTING.md#translations)

### [Bug Report](CONTRIBUTING.md#bug-report)

We use [Github issues][issues] to report new bugs either internals or externals, this way we ensure the issues having a linked Pull Requests and visibility near the code. Before filling a new task, try to make sure your problem doesn't already exist.

If you found a bug, please report it using the [Bug Report template][issue_bug] and answer the questions in it, as far as possible including:

* a detailed explanation of steps to reproduce the error.
* your operating system, browser and version used.
* a screenshot (if it's possible).
* a dev tools console exception stack trace (if it's available).

If you find a security bug, that you would prefer to discuss in private, you can first mail us at [support@stooa.com](mailto:support@stooa.com).

### [Bug Fixing](CONTRIBUTING.md#bug-fixing)

You can explore our [Github's issues][issues] to find bugs. They are classified and explained by the community and the core team.

To fix them just [fork][how_to_fork] this project and create a [Pull Request][how_to_pr] linking the issue.

### [New Features](CONTRIBUTING.md#new-features)

To ask for new features, you will have to open a new issue using the [New Feature template][issue_feature] and answer the questions in it.

### [Third party integration](CONTRIBUTING.md#third-party)

To create a third party integration, open a [new issue on Github][issues] and team will contact you ASAP.

### [Translations](CONTRIBUTING.md#translations)

We are eager to get your help translating Stooa. You just need to access our team of translators with the link below, set up an account in Weblate and start contributing. Join us to make sure your language is covered! [Help Stooa to translate content][weblate]. Please, see our detailed [translation guide][translation] for more information about how to collaborate through Weblate translation platform.

Localization Bugs: Stooa use Weblate to manage the i18n files so don’t submit a pull request to those files. To fix a translation, just access our team of translators, set up an account in the [Stooa Weblate project][weblate] and start contributing. You also might want to take a look at the guide for [Translating using Weblate](https://docs.weblate.org/en/latest/user/translating.html).

## [DCO License](CONTRIBUTING.md#DCO-license)

By submitting code you are agree with the [DCO license][dco_license].
```
    Developer's Certificate of Origin 1.1

    By making a contribution to this project, I certify that:

    (a) The contribution was created in whole or in part by me and I
        have the right to submit it under the open source license
        indicated in the file; or

    (b) The contribution is based upon previous work that, to the best
        of my knowledge, is covered under an appropriate open source
        license and I have the right under that license to submit that
        work with modifications, whether created in whole or in part
        by me, under the same open source license (unless I am
        permitted to submit under a different license), as indicated
        in the file; or

    (c) The contribution was provided directly to me by some other
        person who certified (a), (b) or (c) and I have not modified
        it.

    (d) I understand and agree that this project and the contribution
        are public and that a record of the contribution (including all
        personal information I submit with it, including my sign-off) is
        maintained indefinitely and may be redistributed consistent with
        this project or the open source license(s) involved.
  ```

To sign it you will only have to reply to your own PR to our lovely bot that you accept the License. Cool and lovely bots 🤖 .

[issues]: https://github.com/Runroom/Stooa/issues
[issue_bug]: https://github.com/Stooa/Stooa/issues/new?assignees=&labels=bug%2Ctriage&template=BUG-REPORT.yml&title=%5BBug%5D%3A+
[issue_feature]: https://github.com/Stooa/Stooa/issues/new?assignees=&labels=feature-request&template=FEATURE-REQUEST.yml&title=%5BFeature%5D%3A+
[discussions]: https://github.com/Stooa/Stooa/discussions
[documentation]: https://github.com/Stooa/Documentation
[how_to_fork]: https://help.github.com/articles/fork-a-repo/
[how_to_pr]: https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests
[weblate]: https://hosted.weblate.org/projects/stooa/
[translation]: docs/contributing/translations.md
[dco_license]: https://github.com/Stooa/Documentation/blob/main/DCOLICENSE

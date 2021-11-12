# Translations

Thank you for interest in contribute translating Stooa. Here you will find ways to do it.

## How to become a Stooa translator

We are using [Weblate as translation platform][weblate], so the first thing you need to be a Stooa translator is to have a Weblate account ([you can register here](https://hosted.weblate.org/accounts/register/)).

You also might want to take a look at the guide for [Translating using Weblate](https://docs.weblate.org/en/latest/user/translating.html).

When collaborating with translations, Weblate will automatically create a Pull Request in the project repository with all the translations added.

## Add a new language

To add a language that is still not among the Stooa language options:

* Go to the [components list](https://hosted.weblate.org/projects/stooa/).
* Select the component you want to add the translation.
* Press the "Start new translation" button.
* Choose the language you want to translate to.
* Press the "Start new translation" button at the start new translation page.
* Start translating strings for the new language

![Weblate Components list](../assets/img/translations/weblate-components-list.png)

![Weblate Start new translation button](../assets/img/translations/weblate-component-languages.png)

![Weblate Add new language](../assets/img/translations/weblate-start-translation.png)

## Add a new translation

To add a new translation (a string with a lacking translation for a certain language) follow the next steps:

* Go to the [components list](https://hosted.weblate.org/projects/stooa/).
* Select the component you want to add the translation.
* Click the edit button (pencil icon) close to the name of the language where you want to add the missing translation or translations.
* Find and select the translation's to complete.
* Complete the translation in the required input field.
* Press the "Save" button.
* Repeat the action with as many translation strings you can / you want

![Weblate Component languages](../assets/img/translations/weblate-component-languages.png)

![Weblate Edit translation](../assets/img/translations/weblate-edit-translation.png)

## Change an approved translation

To edit an already approved translation string follow the next steps:

* Go to the [components list](https://hosted.weblate.org/projects/stooa/).
* Select the component you want to add the translation.
* Click the name of the language where is the translation you want to change.
* Click the Browse button.
* Find and select the translation's to complete.
* Change the translation in the input field.
* Press the "Save" button if you have permissions.

![Weblate Component languages](../assets/img/translations/weblate-component-languages.png)

![Weblate Browse translations](../assets/img/translations/weblate-browse-translations.png)

## New Language Request

In the case of adding a new language, a minimum of 80% of the translations of the entire project components is necessary for the Pull Request to be approved. Furthermore, keep in mind that we will also require the 100% of the translation in the "Frontend - App" and "Frontend - Common" components.

Please consider that the creation of a new language requires the action of developers to integrate it into the app. A Pull Request for this development is also needed so that you can make it yourself, and it will be very welcome! :)

If you are not a developer, you can [start a new discussion][new_discussion] inside the "Help wanted" category to ask the developer community for help

[weblate]: https://hosted.weblate.org/projects/stooa/
[new_discussion]: https://github.com/Stooa/Stooa/discussions/new

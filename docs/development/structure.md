# Structure

The [Stooa](https://github.com/Stooa/Stooa) repository contains code for:

## Backend

The `/backend` folder contains all the backend code. We are mainly using [Symfony][symfony] with [Api Platform][api-platform] (for the API generation) and [Sonata][sonata] for the administration panel.

If you change `backend` code, there are several checks that the code need to pass:
* [PHPStan][phpstan]
* [Psalm][psalm]
* [PHP CS FIXER][php-cs-fixer]
* [PHPUnit][phpunit]

## Frontend

The `/frontend` folder contains all the frontend code. We are mainly using [React][react] with [Next.js][next] and
[Apollo][apollo] for the GraphQL calls to the backend.

If you change `frontend` code, there are several checks that the code need to pass:
* [ESLint][eslint] 
* [Prettier][prettier]
* [Next.js build][next]
* [Jest tests][jest]

[symfony]: https://github.com/symfony/symfony
[api-platform]: https://github.com/api-platform/api-platform
[sonata]: https://github.com/sonata-project/SonataAdminBundle
[react]: https://github.com/facebook/react
[next]: https://github.com/vercel/next.js
[apollo]: https://github.com/apollographql
[phpstan]: https://github.com/phpstan/phpstan
[psalm]: https://github.com/vimeo/psalm
[php-cs-fixer]: https://github.com/FriendsOfPHP/PHP-CS-Fixer
[phpunit]: https://github.com/sebastianbergmann/phpunit
[eslint]: https://github.com/eslint/eslint
[prettier]: https://github.com/prettier/prettier
[jest]: https://github.com/facebook/jest

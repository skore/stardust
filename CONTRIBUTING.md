# Contributing

Thanks for your interest in contributing to Ziggy! Contributions are welcome and will be credited.

To keep things running smoothly we ask you to follow a few guidelines when contributing. Please read and understand this contribution guide before creating an issue or pull request.

## Etiquette

Be kind.

## Viability

If you have an idea for a feature, we'd prefer you open a discussion before going to the trouble of writing code. We welcome your ideas, but we'd like to work with you to come up with solutions that work well for the project as a whole. We're usually pretty responsive, so it shouldn't take us long to figure out whether and how best to implement your idea.

## Procedure

Before filing an issue:

- Attempt to replicate the problem, to ensure that it wasn't a coincidence.
- Check to make sure your feature suggestion isn't already present within the project.
- Check the pull requests tab to ensure that your feature or bugfix isn't already in progress.

Before submitting a pull request:

- Check the codebase to ensure that your feature doesn't already exist.
- Check the pull requests to ensure that another person hasn't already submitted the feature or fix.

## Tests

Please write tests for any fixes or new features you contribute. We use [Orchestra Testbench](https://github.com/orchestral/testbench) as our base PHPUnit test for PHP and [Jest](https://jestjs.io/) for testing our JavaScript.

You can run PHP tests with `vendor/bin/phpunit` and JavaScript tests with `npm run test`.

If you need any help with this please don't hesitate to ask.

> If your filesystem uses `CRLF` instead of `LF` line endings (e.g. Windows) you may see errors related to that when running tests. To fix this you can run `git config --global core.autocrlf input` to configure Git to preserve the line endings from the repository when cloning. You may have to clone this repository again.

## Types

TypeScript types are included with Ziggy and maintained manually.

To test the type definitions, open `tests/js/types.ts` in an editor or IDE with TypeScript support. This file contains sample code using Ziggy's `route()` function, and can be used to ensure that specific examples do or don't type-check as expected. To add a test for code that should work, add the code (with a comment explaining its purpose) and verify that it doesn't create any type errors. To add a test for code that should _not_ work, and should generate a type error, add the code with a `// @ts-expect-error` annotation, and verify that without the annotation it generates a type error and with the annotation it doesn't.

See also [`tighten/ziggy-type-testing`](https://github.com/tighten/ziggy-type-testing).

## Requirements

- **[PSR-2 Coding Standard](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)** - The easiest way to apply the conventions is to install [PHP Code Sniffer](https://github.com/squizlabs/PHP_CodeSniffer).
- **Tlint styles** - Tighten-specific styles. Tlint is built for apps, so there are some settings that might not make sense in a package, but [download Tlint](https://github.com/tighten/tlint) and run it on your pull requests to see if it suggests any reasonable changes.
- **One pull request per feature** - If you want to do more than one thing, send multiple pull requests.

# phpnomad/repository-template

Starter scaffold for new PHPNomad packages. It's a GitHub template repo that gives you the standard layout, CI workflows, coding standards, and test setup that every `phpnomad/*` package shares, so a new package starts on the same baseline as the rest of the ecosystem.

## How to use this template

Click the "Use this template" button on the [repository page](https://github.com/phpnomad/repository-template). GitHub will create a new repo in your account or organization with the same file tree and a clean commit history.

You can do the same thing from the command line with `gh`:

```bash
gh repo create my-org/my-new-package \
    --template phpnomad/repository-template \
    --public \
    --clone
```

## What's included

- `lib/` and `tests/` directories for package source and unit tests, with the autoloader and test suite already wired in `composer.json` and `phpunit.xml`.
- GitHub Actions workflow for PHPUnit, running on a matrix of PHP 7.4, 8.0, 8.1, and 8.2.
- GitHub Actions workflow for PHPStan at level 9, scanning `lib/` and `tests/`.
- GitHub Actions workflow for spellcheck using `rojopolis/spellcheck-github-actions`, configured via `.spellcheck.yml` and `.wordlist.txt`.
- Dependabot config that opens daily Composer dependency updates with a `deps` commit prefix.
- A pull request template covering summary, details, testing instructions, and author and reviewer checklists.
- `.php-cs-fixer.dist.php` preconfigured for PSR-12, with a `composer php-cs-fixer` script shortcut.
- `.editorconfig`, `.gitignore`, and an MIT `LICENSE.txt`.

## After you clone

The template ships with placeholder values that need to be replaced once you've created your new repo. Before your first commit:

1. In `composer.json`, update `name`, `description`, `homepage`, and the PSR-4 autoload namespaces to match your new package.
2. Rename the base namespace in any stub files and update the `autoload-dev` namespace to match.
3. Replace this README with one that describes what your package actually does.
4. Add your source files under `lib/` and your tests under `tests/Unit/`.

## License

MIT. See [LICENSE.txt](LICENSE.txt).

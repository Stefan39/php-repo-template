# Contributing

Thanks for your interest. Small, focused changes are the easiest to review.

## Before you start

- Open an issue first for anything bigger than a bug fix or a typo, so we can agree on the approach.
- Issues in English or German are fine. Replies are usually in English.

## Development

```bash
composer install
composer tests        # PHPUnit
composer phpstan      # PHPStan, level 8
composer cs           # php-cs-fixer, dry run
composer cs-fix       # apply code style
```

All three checks must pass; CI runs them on every pull request.

## Pull requests

- Branch from `main`, one topic per pull request.
- Add or update tests for every behavior change.
- Update `CHANGELOG.md` under "Unreleased".
- Commit messages follow Conventional Commits: `feat: ...`, `fix: ...`, `docs: ...`.
- Use `declare(strict_types=1);` in every PHP file.

## Code of conduct

By taking part you agree to the [Code of Conduct](CODE_OF_CONDUCT.md).

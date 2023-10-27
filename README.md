# XIMA GitLab-CI Templates


## Installation

See [.example.yml](.example.yml) for example GitLab-CI configuration.

Use `include` to reference template files:

```yaml
include:
  - project: 'symfony-cms/general/misc/gitlab-ci-templates'
    ref: latest
    file:
      - '/analyse/analyse-composer.yml'
```

Extend and override configuration variables:

```yaml
variables:
  PATH_PROJECT_DIR: "app/"
```

Extend and override further ci jobs.

## Description of all the jobs

### Analyse

| Job name                    | File                                                                     | Description                                                                                |
|-----------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| `analyse:composer:lint`     | [analyse-composer-lint.yml](./analyse/analyse-composer-lint.yml)         | Use composer normalize to lint `composer.json` via `composer run composer:normalize:check` |
| `analyse:composer:security` | [analyse-composer-security.yml](./analyse/analyse-composer-security.yml) | Run composer dependency check via `vendor/bin/dep security:check:composer`                 |
| `analyse:editorconfig`      | [analyse-editorconfig.yml](./analyse/analyse-editorconfig.yml)           | Check editorconfig for project files via `composer run editorconfig:check`                 |
| `analyse:php:cs-fixer`      | [analyse-php-cs-fixer.yml](./analyse/analyse-php-cs-fixer.yml)           | Run php cs fixer to fix regarding coding standards via `composer run php:cs-fixer:check`   |
| `analyse:php:lint`          | [analyse-php-lint.yml](./analyse/analyse-php-lint.yml)                   | Run php lint via `composer run php:lint`                                                   |
| `analyse:php:rector`        | [analyse-php-rector.yml](./analyse/analyse-php-rector.yml)               | Run php rector via `composer run php:rector:check`                                         |
| `analyse:php:stan`          | [analyse-php-stan.yml](./analyse/analyse-php-stan.yml)                   | Run php stan via `composer run php:stan:check`                                             |
| `analyse:xml:lint`          | [analyse-xml-lint.yml](./analyse/analyse-xml-lint.yml)                   | Lint xml files via `composer run xml:lint`                                                 |
| `analyse:yaml:lint`         | [analyse-yaml-lint.yml](./analyse/analyse-yaml-lint.yml)                 | Lint yaml files via `composer run yaml:lint`                                               |


### Build

### Deploy

### Sync

### Test

_ToDo_ further documentation
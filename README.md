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

| Job name                    | Description                          |
|-----------------------------|--------------------------------------|
| `analyse:composer:lint`     | Use composer normalize               |
| `analyse:composer:security` | Run composer dependency check        |
| `analyse:editorconfig`      | Check editorconfig for project files |
| `analyse:php:cs-fixer`      | Run php cs fixer                     |
| `analyse:php:lint`          | Run php lint                         |
| `analyse:php:rector`        | Run php rector                       |
| `analyse:php:stan`          | Run php stan                         |
| `analyse:xml:lint`          | Lint xml files                       |
| `analyse:yaml:lint`         | Lint yaml files                      |


### Build

### Deploy

### Sync

### Test

_ToDo_ further documentation
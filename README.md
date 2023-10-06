# XIMA GitLab-CI Pipeline

## How to use in project

1. Create .gitlab-ci.yml file with following content

```
include:
    - project: 'symfony-cms/general/misc/pipeline'
      ref: v0.0.1
      file: '/gitlab-ci.yml'
#-----------------------------------------------------------------------------------------------------------------------
# CONFIGURATION
#-----------------------------------------------------------------------------------------------------------------------
variables:
    # Stage
    SSH_USER_STAGE: "xima"
    HOST_STAGE: ""
    SSH_HOST_STAGE: ""
    
    # Prod
    SSH_USER_PROD: ""
    HOST_PROD: ""
    APP_URL_PROD: ""
    SSH_HOST_PROD: ""

#-----------------------------------------------------------------------------------------------------------------------
# JOBS
#-----------------------------------------------------------------------------------------------------------------------

# Define feature branch pattern
.feature-branches:
    only:
        - /^release-(.*)/
        - /^feature-.*$/
        - /^SCI-.*$/
        - main
 
```
Fill in credentials and set ref: to latest stable release.

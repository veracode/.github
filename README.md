# Policy templates

Workflow templates shared across projects.

## Usage

`policyscan.yml` and `policyscan-java.yml` - These templates perform an Upload and Scan (Policy Scan) are differentiated only by how they package the code for the policy scan. Each has required inputs that must be set in the repo's secrets to run successfully:

- `VERACODE_API_ID` - API ID to be used when performing upload and scan
- `VERACODE_API_KEY` - API Key to be used when performing upload and scan
- `VERACODE_APP_ID` - set if you want to pass the app ID along with the pipeline scan request

`sca.yml` - This template performs a very basic SCA Agent scan with auto pull request. Required secrets include:
- `SRCCLR_API_TOKEN` - generated when creating a new integration under the Agents tab
-  `SCM_GITHUB` - See instructions in the [Github documentation](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token).
- `USER_EMAIL` - email address, used in pull requests
- `USER_NAME` - username, used in pull requests

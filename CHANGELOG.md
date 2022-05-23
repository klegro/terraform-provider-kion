# Changelog

All notable changes to this project will be documented in this file.

## [0.3.1] - 2022-02-25
### Changed
- Fix the description for IAM policies in the documentation to be more accurate.

## [0.3.0] - 2022-02-25
### Added
- Support creating, updating, and deleting resources for: AWS Service Control Policies.
- Support adding and removing AWS Service Control Policies on Project and OU Cloud Rules.
- Support creating, updating, and deleting resources for: Azure ARM Templates.
- Support adding and removing Azure ARM Templates on Project and OU Cloud Rules.
- Support creating, updating, and deleting resources for: Azure Role Definitions.
- Support adding and removing Azure Role Definitions on Project and OU Cloud Rules.

### Changed
- Rebrand from cloudtamer.io to Kion.
- Change provider name: `cloudtamer-io/cloudtamerio` to `kionsoftware/kion`.
- Change resource and data source names prefix: `cloudtamer_` to `kion_`.
- Change environment variables: `CLOUDTAMERIO_URL` and `CLOUDTAMERIO_APIKEY` to `KION_URL` and `KION_APIKEY`, respectively.
- Made the `created_by_user_id` field for Compliance Checks optional. This field will default to the requesting user's ID if not specified.

## [0.2.0] - 2021-11-19
### Added
- Support creating, updating, and deleting resources for: user groups.
- Support creating, updating, and deleting resources for: SAML IDMS user group associations.
- Support creating, updating, and deleting resources for: Projects
- Support creating, updating, and deleting resources for: Google Cloud IAM Roles.
- Support adding and removing Google Cloud IAM Roles on Project and OU Cloud Rules.

### Changed
- Fix several requests that use the wrong user & user group IDs to remove owners from a resource.

## [0.1.4] - 2021-08-09
### Added
- Support creating, updating, and deleting resources for: OUs. (Requires Kion v2.31.0 or newer)

## [0.1.3] - 2021-06-29
### Changed
- Fix bug on project cloud access role creation so 'apply_to_all_accounts' and 'accounts' fields are mutually exclusive.
- Remove unused errors throughout the code.

## [0.1.2] - 2021-04-01
### Added
- Support creating, updating, and deleting resources for: OU cloud access roles and project cloud access roles.

### Changed
- Fix bug on compliance standard creation so compliance checks are attached during creation instead of requiring another `terraform apply`.
- Fix bug on cloud rule creation so associated items are attached during creation instead of requiring another `terraform apply`.

## [0.1.1] - 2021-03-30
### Added
- Ability to import resources using `terraform import`.

## [0.1.0] - 2021-02-08
### Added
- Initial release of the provider.
- Support creating, updating, and deleting resources for: AWS CloudFormation templates, AWS IAM policies, Azure policies, cloud rules, compliance checks, and compliance standards.
- Support querying data sources for: AWS CloudFormation templates, AWS IAM policies, Azure policies, cloud rules, compliance checks, and compliance standards.
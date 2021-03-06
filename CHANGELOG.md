## v0.5.2 (Unreleased)

ENHANCEMENTS:

* resource/auth0_user: `name`, `family_name`, `given_name`, `blocked` and `picture` are added ([#166](https://github.com/alexkappa/terraform-provider-auth0/pull/166))


## v0.5.1 (January 22, 2020)

BUG FIXES:

* resource/auth0_email: fix `api_key` issue when reading back the resource from Auth0 ([#161](https://github.com/alexkappa/terraform-provider-auth0/issues/161))

## v0.5.0 (January 20, 2020)

ENHANCEMENTS:

* resource/auth0_email: add `domain` field to allow configuring of mailgun provider ([#164](https://github.com/alexkappa/terraform-provider-auth0/pull/164))

NOTES:

* Upgrade to `gopkg.in/auth0.v3` (`v3.0.3`)


## v0.4.3 (January 16, 2020)

BUG FIXES:

* resource/auth0_client_grant: fix empty scope issue ([#162](https://github.com/alexkappa/terraform-provider-auth0/pull/162))

## v0.4.2 (December 30, 2019)

ENHANCEMENTS:

* resource/*: update and destroy operations now do not fail if the resource has been deleted manually ([#155](https://github.com/alexkappa/terraform-provider-auth0/pull/155)).

## v0.4.1 (December 18, 2019)

ENHANCEMENTS:

* resource/auth0_client: support rotating `client_secret` by changing the value of `client_secret_rotation_trigger` ([#153](https://github.com/alexkappa/terraform-provider-auth0/pull/153)).

## v0.4.0 (December 13, 2019)

ENHANCEMENTS:

* resource/auth0_connection: Introduce `password_complexity_options` ([#132](https://github.com/alexkappa/terraform-provider-auth0/pull/132)).
* resource/auth0_resource_server: `signing_secret` is now also a computed field. If set it's validated to be at least 16 characters ([#146](https://github.com/alexkappa/terraform-provider-auth0/pull/146)).
* resource/auth0_resource_server: `identifier` update forces new resource ([#147](https://github.com/alexkappa/terraform-provider-auth0/pull/147)).
* resource/auth0_role (**breaking change**): `user_ids` is removed. In its place the following is introduced ([#149](https://github.com/alexkappa/terraform-provider-auth0/pull/149)).
* resource/auth0_user: `roles` is added ([#149](https://github.com/alexkappa/terraform-provider-auth0/pull/149)).

BUG FIXES:

* resource/auth0_connection: Fix `password_dictionary` [#128](https://github.com/alexkappa/terraform-provider-auth0/pull/128)
* resource/auth0_client: Fix `is_first_party` setting if set to zero value ([#148](https://github.com/alexkappa/terraform-provider-auth0/pull/148)). 

## v0.3.1 (December 10, 2019)

ENHANCEMENTS:

* resource/auth0_tenant: Support `flags` and `universal_login` settings [#133](https://github.com/alexkappa/terraform-provider-auth0/pull/133)

## v0.3.0 (December 10, 2019)

BUG FIXES:

* resource/auth0_email_template: Fix 404 issue when modifying templates ([#144](https://github.com/alexkappa/terraform-provider-auth0/pull/144)).

NOTES:

* Upgrade to `gopkg.in/auth0.v2`

## v0.2.2 (December 10, 2019)

ENHANCEMENTS:

* Switch to using Github Actions in favour of Wercker.

## v0.2.1 (October 21, 2019)

ENHANCEMENTS:

* resource/auth0_connection: Improved support for `enabled_clients` by using a set instead of a list ([#105](https://github.com/alexkappa/terraform-provider-auth0/pull/105)).
* resource/auth0_connection: Add `community_base_url` to `salesforce-community` type connections ([#130](https://github.com/alexkappa/terraform-provider-auth0/pull/130)).
* resource/auth0_client: Validate `app_type` ([#112](https://github.com/alexkappa/terraform-provider-auth0/pull/)).
* resource/auth0_user: Make `password` a sensitive field ([#117](https://github.com/alexkappa/terraform-provider-auth0/pull/117)).

BUG FIXES

* resource/auth0_connection: Fix incorrect schema for `password_no_personal_info` ([#107](https://github.com/alexkappa/terraform-provider-auth0/pull/107)).
* resource/auth0_user: Fix bugs in `user_metadata`, `app_metadata` and `password` ([#131](https://github.com/alexkappa/terraform-provider-auth0/pull/131)).

NOTES:

* Improve documentation on supported features ([#113](https://github.com/alexkappa/terraform-provider-auth0/pull/113)).
* Update examples after upgrade to 0.2.x ([#114](https://github.com/alexkappa/terraform-provider-auth0/pull/114)).
* Update terraform and auth0 dependencies to latest release ([#120](https://github.com/alexkappa/terraform-provider-auth0/pull/120)).
* Add tenant example ([#125](https://github.com/alexkappa/terraform-provider-auth0/pull/125)).

FEATURES:

* resource/auth0_user: Support for `nickname` attribute ([#108](https://github.com/alexkappa/terraform-provider-auth0/pull/108))

## v0.2.0 (June 27, 2019)

ENHANCEMENTS:

* resource/auth0_user: Add support for user attribute `nickname`

BUG FIXES:

* resource/auth0_connection: Fix icorrect schema of `password_no_personal_info`

NOTES:

* Provider is compatible with Terraform v0.12.3

## v0.1.20 (May 17, 2019)

FEATURES:

* resource/auth0_connection: Add twillio for guardian mfa

## v0.1.19 (May 14, 2019)

ENHANCEMENTS

* resource/auth0_connection: Add `adfs_server` field.

## v0.1.18 (March 26, 2019)

NOTES:

* Extract version from changelog for release notes.

## v0.1.17 (March 26, 2019)

NOTES:

* Update Travis to build on tag push.

## v0.1.16 (March 25, 2019)

NOTES:

* Added contributing, code of conduct, issue templates to the project.

## v0.1.15 (March 25, 2019)

FEATURES:

* **New Resource:** auth0_tenant ([#79](https://github.com/alexkappa/terraform-provider-auth0/pull/79))

ENHANCEMENTS:

* resource/auth0_connection: `enabled_clients` will suppress diff if the list order is different.
* resource/auth0_connection: set `client_secret` to sensitive ([#91](https://github.com/alexkappa/terraform-provider-auth0/pull/91)).
* resource/auth0_resource_server: introduce `token_lifetime_for_web` ([#84](https://github.com/alexkappa/terraform-provider-auth0/pull/84)).

NOTES:

* Re-imported Auth0 SDK from `gopkg.in/auth0.v1`.

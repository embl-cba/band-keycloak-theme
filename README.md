# BAND Keycloak login theme

Login theme of the BAND portal's Keycloak (realm `eosc`), for Keycloak 26.
Install it as `themes/eosc-login-theme/` (the name the realm uses) and set it
as the realm's login theme.

- `login/login.ftl`: the identity-provider buttons (Google, LS AAI) only;
  username/password login and self-registration are off in the realm.
- `login/template.ftl`: page frame with the EMBL, EuBI, BAND and de.NBI logos
  and the privacy/terms links. Keycloak's own login pages (errors, review
  profile, ...) use it too; the layout macro accepts their Keycloak 26
  parameters (`displayRequiredFields`, `showAnotherWayIfPresent`).
- `login/messages/`, `login/resources/`: texts, CSS, images.

Based on the EOSC-Life theme (git.embl.de grp-cbbcs/keycloak-theme-eosc-life)
as deployed with Keycloak 4.5; only the files the pages use are kept.
Bundled: Bootstrap 4.1.0 (MIT) and Font Awesome Free 5.0.10 (icons CC BY 4.0,
code MIT).

The BAND deployment ([embl-cba/band](https://github.com/embl-cba/band), role
`keycloak`) builds it from a tag of this repository into its Keycloak image.

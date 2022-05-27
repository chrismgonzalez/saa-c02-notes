# Object Versioning

Object versioning is controlled at a bucket level.  It starts as disabled, once enabled you can no longer disable.  However you can suspend the versioning, and then enable it again.

Versioning lets you store *multiple versions* of objects within a bucket.  Operations which would modify objects *generate a new version.*

## MFA Delete

* Enabled in *versioning configuration*
* MFA is required to change bucket *versioning state*
* MFA is required to *delete versions*
* Serial Number (MFA) + code passed with API CALLS

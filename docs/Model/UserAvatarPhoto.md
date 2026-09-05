# # UserAvatarPhoto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**photo** | **string** | Base64 of the raw image bytes — see {@see User::getAvatarPhoto()} for why text rather than a BLOB. | [optional] [readonly]
**type** | **string** | The media type sniffed from the bytes ({@see \\App\\Service\\DirectoryPhoto}), nullable like the old &#x60;avatar_photo_type&#x60; column was: bytes can be stored without a type, and {@see \\App\\Controller\\AvatarController} falls back to &#x60;application/octet-stream&#x60;. | [optional]
**id** | **string** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

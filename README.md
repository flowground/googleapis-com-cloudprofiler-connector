# ![LOGO](logo.png) Stackdriver Profiler **flow**ground Connector

## Description

A generated **flow**ground connector for the Stackdriver Profiler API (version v2).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/cloudprofiler/v2/swagger.json<br/>
Generated at: 2019-05-23T12:13:06+03:00

## API Description

Manages continuous profiling information.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### UpdateProfile updates the profile bytes and labels on the profile resource<br/>
> created in the online mode. Updating the bytes for profiles created in the<br/>
> offline mode is currently not supported: the profile content must be<br/>
> provided at the time of the profile creation.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Output only. Opaque, server-assigned, unique ID for this profile.
* `updateMask` - _optional_ - Field mask used to specify the fields to be overwritten. Currently only
profile_bytes and labels fields are supported by UpdateProfile, so only
those fields can be specified in the mask. When no mask is provided, all
fields are overwritten.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### CreateProfile creates a new profile resource in the online mode.<br/>
> <br/>
> The server ensures that the new profiles are created at a constant rate per<br/>
> deployment, so the creation request may hang for some time until the next<br/>
> profile session is available.<br/>
> <br/>
> The request may fail with ABORTED error if the creation is not available<br/>
> within ~1m, the response will indicate the duration of the backoff the<br/>
> client should take before attempting creating a profile again. The backoff<br/>
> duration is returned in google.rpc.RetryInfo extension on the response<br/>
> status. To a gRPC client, the extension will be return as a<br/>
> binary-serialized proto in the trailing metadata item named<br/>
> "google.rpc.retryinfo-bin".

*Tags:* `projects`

#### Input Parameters
* `parent` - _required_ - Parent project to create the profile in.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### CreateOfflineProfile creates a new profile resource in the offline mode.<br/>
> The client provides the profile to create along with the profile bytes, the<br/>
> server records it.

*Tags:* `projects`

#### Input Parameters
* `parent` - _required_ - Parent project to create the profile in.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-cloudprofiler-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

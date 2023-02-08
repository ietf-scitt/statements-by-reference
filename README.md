# statements-by-reference
Exploration of content reference formats


Seems like in general, we are replacing a `cty` with a media type for a content identifier for a `cty`...

For example:

https://www.iana.org/assignments/media-types/application/spdx+json


One option:

`application/spdx+json` -> `application/spdx+json; content-id=sha256`
`application/spdx+json` -> `application/spdx+json; content-id=shake256`
`application/spdx+json` -> `application/spdx+json; content-id=multicodec`

Then the "content-id" bytes, are the payload.

We should avoid creating a "media type" for a document that "contains content identifiers".

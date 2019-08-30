# funding-schema

JSON schema for open software project funding resources

## Example

```json
{
  "project": "https://github.com/kemitchell/funding-schema.json",
  "contributors": [
    {
      "name": "npm, Inc.",
      "type": "organization",
      "homepage": "https://npmjs.com",
      "updated": "2019-08-30",
      "links": [
        "https://npmjs.com/enterprise"
      ]
    },
    {
      "name": "Kyle E. Mitchell",
      "type": "person",
      "homepage": "https://kemitchell.com",
      "updated": "2019-08-30",
      "links": [
        "https://kemitchell.com/fund"
      ]
    }
  ]
}
```

Funding resources can also incorporate resources for specific contributors by reference:

```json
{
  "project": "https://github.com/kemitchell/funding-schema.json",
  "contributors": [
    {
      "name": "npm, Inc.",
      "type": "organization",
      "homepage": "https://npmjs.com",
      "updated": "2019-08-30",
      "links": [
        "https://npmjs.com/enterprise"
      ]
    },
    { "uri": "https://kemitchell.com/funding.json" }
  ]
}
```

## API

This package exports a JSON schema for funding objects.

The `definitions` property of the schema contains all sub-schemas that you might like to load individually:

- `project`
- `contributor`
- `contributorReference`

This package treats the exposure of those sub-schemas as part of its public API for semantic versioning.

You can validate data against the schema using libraries like [ajv](https://www.npmjs.com/package/ajv).

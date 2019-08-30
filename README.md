# funding-schema

JSON schema for open software project funding resources

## Examples

```json
{
  "project": "https://standardjs.com",
  "contributors": [
    {
      "name": "Feross Aboukhadijeh",
      "type": "person",
      "homepage": "https://feross.org",
      "updated": "2019-08-30",
      "links": [
        "https://www.patreon.com/feross",
        "https://feross.org/support/"
      ]
    }
  ]
}
```

```json
{
  "project": "https://jquery.com",
  "contributors": [
    {
      "name": "JS Foundation",
      "type": "organization",
      "homepage": "https://js.foundation",
      "updated": "2019-08-30",
      "links": [
        "https://js.foundation/about/donate"
      ]
    }
  ]
}
```

```json
{
  "project": "https://babeljs.io",
  "contributors": [
    {
      "name": "OpenCollective",
      "type": "organization",
      "homepage": "https://opencollective.com/babel",
      "updated": "2019-08-30",
      "links": [
        "https://opencollective.com/babel/contribute"
      ]
    }
  ]
}
```

```json
{
  "project": "https://github.com/chalk/chalk",
  "contributors": [
    {
      "name": "Tidelift",
      "type": "organization",
      "homepage": "https://tidelift.com/",
      "updated": "2019-08-30",
      "links": [
        "https://tidelift.com/subscription/pkg/npm-chalk"
      ]
    }
  ]
}
```

```json
{
  "project": "https://github.com/kemitchell/funding-schema.json",
  "contributors": [
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

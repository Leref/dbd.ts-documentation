# Contributing
You contribute to the DBD.TS documentation by making a [pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

Make sure to follow the [Proper Wiki Structure](#proper-wiki-structure) when contributing.

   
## Terms and Guidelines
- The name of files must be in the format of `filename.md`. No spaces or special characters (e.g `$`).
- Do not make duplicates or useless pull requests.
- Fact-check/verify information included in the pull request.

## Proper Wiki Structure
### Grammar
- Don't use gendered pronouns (e.g. she/her/hers/he/him/his). Instead use: They, them, their.
```diff
- He is cool.
+ They are cool.
```
- Use "we" instead of "I" when referring to yourself.
```diff
- If you use the `$eval` function, I strongly recommend you also use `$onlyForIDs`.
+ If you use the `$eval` function, we strongly recommend you also use `$onlyForIDs`.
```
- "You"/"your" instead of "we"/"our"
```diff
- We can get our bot's ID using `$botID`.
+ You can get your bot's ID using `$botID`.
```
- Avoid using these phrases:
```diff
- dumb, weird, stupid, ugly, uneeded, useless, bad, deadly, noob, trash, suck, I don't know, I don't care, idiot
```

### Shortening Headers
Make headers are short as possible, and in [title case](https://www.dummies.com/wp-content/uploads/410813.image0.jpg).

```diff
- ## How to create embeds
+ ## Creating Embeds
```

### Field Tables
```
This function has ... field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| field1| description | type | boolean |
| field2| description | type | boolean |
```
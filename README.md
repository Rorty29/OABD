# OABD Github guidelines

## General Syntax & Examples

### Whitelist:
```
"UserId": [
  number(WhitelistLevel),
  string?(ChatTag)
]
```

### Stand Whitelist:
```
"StandId": number(WhitelistLevel)
```

### Ganglist:
```
"GroupId": [
  "Title",
  [number, number, number]
]
```

### BanWL:
```
"UserId"
```

### AdonisWhitelist:
```
"Rank": [
  "Level": number,
  "Users": [number(UserId), ...]
]
```

## General Mistakes

This is really basic stuff.
Leaving a comma at the end of the list = DEAD GAME
```
Example of mistake in syntax:

"A": [
  "Level": number,
  "Users": [2, ...],
],

"B": [
  "Level": number,
  "Users": [1, ...]
],

Here the line `"Users": [2, ...],` will brick the json file because the comma is left at the end of the list.
Same will happen with the last line `],` of list B, since it's the last element in the json file.
```

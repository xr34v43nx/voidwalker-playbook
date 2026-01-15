# Goal

The password is stored somewhere on the server with the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## What to learn

How to navigate and search recursively throughout the entire server for certain properties to return the result desired.

### Tools of use
- find

### Added notes:

To clear out a lot of the noise we can use a redirect `2>/dev/null` so only the result wanted is displayed.

`2>` - redirects the stderr(standard error), includes permission errors generated during traversal.
`/dev/null` - where it is directed to
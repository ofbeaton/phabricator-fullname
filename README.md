# phabricator-fullname
Unofficial patch to display Fullnames beside usernames in Phabricator.

Often useful when importing users from a corporate LDAP where the usernames are auto-generated `txf032` etc.

## Installing

```
cd phabricator
git apply fullname.patch
```

## Creating

Aim to make the less changes possible. This is why we only replace `getName` with `getFullname` instead of removing the whole case statement.

Checkout Phabricator. Make two copies of the `phabricator` subdir, `a` and `b`. Make your changes to `b`.

```
git patch a b > fullname.patch
```

Send in a PR, please make sure to include from what date onwards it is good for.

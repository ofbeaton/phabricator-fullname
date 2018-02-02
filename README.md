# phabricator-fullname
Display Fullnames beside usernames in Phabricator

## Installing

```
cd phabricator
git apply fullname.patch
```

## Creating

Checkout Phabricator. Make two copies of the `phabricator` subdir, `a` and `b`. Make your changes to `b`.

```
git patch a b > fullname.patch
```

Send in a PR, please make sure to include from what date onwards it is good for.

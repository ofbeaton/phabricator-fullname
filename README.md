# phabricator-fullname
Unofficial patch to display Fullnames (realname) beside usernames in Phabricator.

Often useful when importing users from a corporate LDAP where the usernames are auto-generated `txf032` etc.

## Updates

The project is considered in a usable state and feature complete.

This project is used in corporate applications. As such, the authors are unlikely to update it on a regular basis, but instead when the corporate applications that use it run into problems. You should expect updates in the 5-10yr range. 

Issues and PRs will be monitored, and we will continue to work with the community to provide updates as they are contributed.

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

## Upstream

As of [2017-01-08](https://secure.phabricator.com/T10598) there is no interest from upstream in providing this as an option. Phacility instead recommends you maintain a patch yourself. This is that patch.

# gpg-demo

A demo on using gpg

## Getting Started

Create keys for Curiola / support@curiola.com

```bash
$ brew install gpg
...
$ gpg --gen-key
gpg (GnuPG) 2.2.4; Copyright (C) 2017 Free Software Foundation, Inc.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

gpg: directory '/Users/nickglynn/.gnupg' created
gpg: keybox '/Users/nickglynn/.gnupg/pubring.kbx' created
Note: Use "gpg --full-generate-key" for a full featured key generation dialog.

GnuPG needs to construct a user ID to identify your key.

Real name: Curiola
Email address: support@curiola.com
You selected this USER-ID:
    "Curiola <support@curiola.com>"

Change (N)ame, (E)mail, or (O)kay/(Q)uit? O
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: /Users/nickglynn/.gnupg/trustdb.gpg: trustdb created
gpg: key 82D872FA6A516A53 marked as ultimately trusted
gpg: directory '/Users/nickglynn/.gnupg/openpgp-revocs.d' created
gpg: revocation certificate stored as '/Users/nickglynn/.gnupg/openpgp-revocs.d/86C5C9ED0F1E3C45C7B174A182D872FA6A516A53.rev'
public and secret key created and signed.

pub   rsa2048 2018-01-19 [SC] [expires: 2020-01-19]
      86C5C9ED0F1E3C45C7B174A182D872FA6A516A53
uid                      Curiola <support@curiola.com>
sub   rsa2048 2018-01-19 [E] [expires: 2020-01-19]
```

Export the keys for usage:

```bash
$ gpg --export "Curiola" > pubring.gpg
$ gpg --export-secret-keys support@curiola.com > secretkey.gpg
...
```

Run the demo:

```bash
$ demo-gpg
... MAGIC!!! ...
```

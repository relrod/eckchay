# eckchay

Yes, the name is pig-latin for "check." Yes, really. No, I am not sorry. :-P

Eckchay is (will be) a system that is, conceptually, rather simple.

You have a list of URLs that you want to watch for changes. You want to
define how to check for those changes (should we check ETag? sha/md5 hash of
content? `Last-Modified`?).

Eckchay watches a list of websites until one changes based on the criteria, at
which point it gets dropped from the list.

To start with, Eckchay will perform checks hourly, though in the future, it
would be nice to have the delay on a per-site basis.

State is stored in a plaintext JSON file and consists of:

- last fetched values for whatever we are checking (ETag, hash, headers, etc)
- epoch timestamp of last fetch
- the relevant url

# License

BSD-3.

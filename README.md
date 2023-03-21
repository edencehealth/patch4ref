# patch4ref

This utility is for running patch scripts based on a `GIT_REF` environment variable. It supports semver naming so if you have a patch called `v1.2.sh` or `v1.sh` and a `GIT_REF` of `v1.2.3`, the patch will be run.

## patch4ref usage

```
Usage: patch4ref [-h|--help] [--strict] [--patch-dir PATCH_DIR] [--git-ref GIT_REF]

The program evaluates the GIT_REF environment variable
(or the "--git-ref GIT_REF" cli argument). For the given GIT_REF,
this program applies patches to the source code to make the container
work (or work better). The GIT_REF can be in any of these formats:

* refs/tags/v2.12.1
* 2.12.1
* v2.12.1
* v2.12
* v2

If given the --strict flag, the program will exit non-zero if no patch
was found for the given git ref.
```

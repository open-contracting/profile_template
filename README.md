# OCDS for TODO

## Getting started

A profile is also an extension. See the [standard_extension_template](https://github.com/open-contracting/standard_extension_template) for how to use this template as an extension. As a profile:

1. [Download a ZIP file version of the template](https://github.com/open-contracting/standard_profile_template/archive/master.zip)
1. Extract it, and initialise it as a git repository (`git init`)
1. Replace `TODO` in `extension.json`, `docs/conf.py`, `docs/index.md`, `docs/_templates/layout.html` and this file
1. Update and prepare any files
1. Commit the files you added or changed
1. Delete `.keep` files once new files are added to those directories (see below)
1. Delete any root `*-schema.json` or `codelists/*.csv` files you didn't change
1. Push to a new public Git repository

```shell
git rm assets/.keep docs/_static/.keep docs/extensions/codelists/.keep locale/.keep schema/codelists/.keep
git commit -am "Remove dummy files"
```

### Updating build-related files

Periodically update the following files across the standard and profiles:

```shell
curl -O https://raw.githubusercontent.com/open-contracting/standard_profile_template/master/common-requirements.txt
curl -O https://raw.githubusercontent.com/open-contracting/standard_profile_template/master/Makefile
curl https://raw.githubusercontent.com/open-contracting/standard_profile_template/master/include/common.mk -o include/common.mk
curl https://raw.githubusercontent.com/open-contracting/standard_profile_template/master/include/prologue.mk -o include/prologue.mk
```

Periodically compare the configurable files to the template's files:

* <https://github.com/open-contracting/standard_profile_template/blob/master/.travis.yml>
* <https://github.com/open-contracting/standard_profile_template/blob/master/docs/conf.py>
* <https://github.com/open-contracting/standard_profile_template/blob/master/include/config.mk>
* <https://github.com/open-contracting/standard_profile_template/blob/master/schema/apply-extensions.py>

## Notes

* The `.tx/config` file was generated by `sphinx-intl create-txconfig`
* The `docs/conf.py` file was generated by `sphinx-quickstart` with the non-default answers:
  * Root path for the documentation: `docs`
  * Project name: `OCDS for TODO`
  * Author name(s): `Open Contracting Partnership`
  * Project version: `1.0`
  * Project release: `1.0-rc.1`
  * Source file suffix: `.md`

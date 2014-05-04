# imgadm(5) -- Manage SmartOS virtual machine images

## DESCRIPTION

This manual page describes file formats used my `imgadm`.

## MANIFEST FORMAT
A dataset manifest is a set of static metadata for the dataset. It is typically
in the form of a JSON ".dsmanifest" file.

The properties are:

* **uuid** (required): unique identifier for the dataset.
* **cloud_name**: identifies from which dataset repository this dataset
  originated.
* **creator_uuid**: identifies the creator of the dataset.
* **creator_name**: is the "login" name for the `creator_uuid`.
* **name** (required): is a short name for the dataset. It may only contain
  ASCII letters, numbers, hypens ('-'), periods ('.') and underscores ('_')
  and it must start with a letter. While capital letters are allowed, they are
  discouraged. The name is case-sensitive and is limited to 32 characters.
* **version** (required): is a short version string for the dataset. It may
  only contain ASCII letters, numbers, hypens ('-'), periods ('.') and
  underscores ('_'). While not enforced, it is strongly encouraged that dataset
  authors use the "X.Y.Z" semantic versioning scheme described at
  http://semver.org/. The version is limited to 32 characters.

## SEE ALSO

    vmadm(1m)

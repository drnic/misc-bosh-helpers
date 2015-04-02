Miscellaneous BOSH helper scripts
=================================

manifest_bosh_info.sh
---------------------

Looks up the `director_uuid` from the target manifest in your `~/.bosh_config` and runs `bosh status` against the matching BOSH director.

```
$ ./bin/manifest_bosh_info.sh test/manifests/cf-bosh-lite.yml
```

find_manifests.sh
-----------------

Finds any BOSH deployment manifests within target path and subfolders.

```
$ ./bin/find_manifests.sh
./test/manifests/cf-bosh-lite.yml

$ ./bin/find_manifests.sh test
./test/manifests/cf-bosh-lite.yml
```

find_manifests_for_release.sh
-----------------------------

Finds BOSH manifests within target path and subfolders that use specified release name

```
$ ./bin/find_manifests_for_release.sh cf
./test/manifests/cf-bosh-lite.yml

$ ./bin/find_manifests_for_release.sh cf test/manifests
./test/manifests/cf-bosh-lite.yml

$ ./bin/find_manifests_for_release.sh xxx
<nofiles>
```

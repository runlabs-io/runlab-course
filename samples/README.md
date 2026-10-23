# Samples that are not labs yet

The catalog finds a lab in a top-level folder that has an `index.md`. These two are kept one level down on purpose, so a connected repository does not see them and a refresh does not build their disks:

- `directives` and `layout` share one disk (`disk_name: directives`, built from `directives/data/`).

`nginx` has its own disk and a snapshot, and was moved back to the top level on 2026-10-23 so it is a lab in the catalog again (staging's sets name it).

Building a disk is a few minutes of the builder and several gigabytes of scratch, so a lab with its own disk is moved back to the top level (`git mv samples/<lab> <lab>`) when it is ready to be a published lab. The labs at the top level use the shared default disk and need no build.

# Samples that are not part of the course

The catalog finds a lab in a top-level folder that has an `index.md`. The labs here are kept one level down on purpose, so a connected repository does not see them and a refresh does not build their disks. The course is the labs at the top level.

- `directives` and `layout` share one disk (`disk_name: directives`, built from `directives/data/`).
- `nginx` has its own disk and a snapshot.
- `alerts`, `basics`, `capture`, and `docker` are labs that are not part of the course.

Building a disk is a few minutes of the builder and several gigabytes of scratch. When a sample is ready to be a published lab, move it to the top level (`git mv samples/<lab> <lab>`), then publish it. A lab moved out of `samples/` has to be published again in the catalog.

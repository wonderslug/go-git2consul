# TODO

## Initial version requirements:
* [x] Better error handling of goroutines through errCh
* [x] Possible usage of a runner to abstract git operations from the consul package
* [] Update on KV should be for modified and deleted files only
* [] Test coverage
* [] Better CI pipeline
* [] Webhook polling

## Future additions:
* File format backend
* Improve on mutex locks
* Run -once flag
* Support for source_root and mountpoint
* Support for tags as branches

## Bugs/Issues:
* [x] Need to update diffs on the KV side
  * This includes only updating changed files
  * Delete untracked files
* [x] If repositories slice is empty, stop the program
* [] Directory check has to check if it's a repository first

## Error handling:
* Better error handling on Loadrepos()
  * Bad configuration should be ignored

## Repo delta KV handling:
* [x] On added, modified: PUT KV
* [x] On delete: DEL KV
* [x] On rename: DEL old KV followed by PUT new KV
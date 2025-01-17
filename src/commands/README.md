This directory contains JSON files, one for each command.

Each JSON contains all the information about the command itself, but these JSON files are not to be used directly!
Any third party who needs access to command information must get it from `COMMAND INFO` and `COMMAND DOCS`.
The output can be extracted in a JSON format by using `valkey-cli --json`, in the same manner as in `utils/generate-commands-json.py`.

The JSON files are used to generate commands.def within this repo and JSON files for documentation, and
despite looking similar to the output of `COMMAND` there are some fields and flags that are implicitly populated, and that's the
reason one shouldn't rely on the raw files.

The `reply_schema` section is a standard JSON Schema (see https://json-schema.org/) that describes the reply of each command.
It is designed to someday be used to auto-generate code in client libraries, but is not yet mature and is not exposed externally.


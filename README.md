# Task

A simple build system executing tasks written in Bash, JavaScript, TypeScript, or Python.

## Usage

Tasks can be written in Bash, JavaScript, Typescript, and Python and are located in `./tasks/some/command/task{.sh,.js,.ts,.py}`.
Execute a task as follows.
On Windows, execute it using, e.g., Git Bash.

```shell linenums="1"
./task [task] <...arguments> 
```

For example, the following example command simply echos your arguments using a Task written in Bash.

```shell linenums="1"
./task echo:sh hello world
```

Note, we assume that `bash`, `node`, `node-ts`, and `python` are in `PATH`.

## Writing Tasks

The following environment variables are available inside tasks.

| Environment   | Description                                                      | 
|---------------|------------------------------------------------------------------| 
| TASK_BINARY   | The absolute path of `./task`.                                   | 
| TASK_ROOT_DIR | The absolute path of the root directory of the project.          | 
| TASK_TASK_DIR | The absolute path of the directory in which the task is located. |

Some hints:

- There is no need to include `#!/usr/bin/bash` or `set -e` in Bash tasks.
- Tasks are executed from `TASK_ROOT_DIR`.
- Always add a new line at the end of every file.

## Similar Projects

It is worth to check out the following projects.

- https://github.com/labaneilers/bs
- https://github.com/jnider/bake
- https://github.com/8gears/do
- https://github.com/go-task/task

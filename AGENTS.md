# Contributing with AI agents

PyCodeUpdate uses additional AI resources to provide project context and task-specific guidance.

## AI resources

The `.agents/` directory contains Git submodules:

* `.agents/context/` — project knowledge, architecture, conventions, decisions, and other context
* `.agents/skills/` — task-specific skills, workflows, and instructions

If the submodules are not initialized, run:

```bash
git submodule update --init --recursive
```

Read the relevant context and skills before making changes when they apply to the task. **Do not assume project-specific conventions when the available resources can provide the answer.**

## Using context and skills

* Use `context` to understand how PyCodeUpdate is structured and why it works the way it does.
* Use `skills` when a task has a corresponding skill or workflow.
* Read only the resources relevant to the current task when possible.
* Treat project-specific guidance as higher priority than generic assumptions or preferences.
* If resources conflict with the existing codebase, inspect the surrounding implementation and determine the appropriate approach before making changes.
* Do not modify `.agents/` resources unless the task specifically requires changes to the AI resources themselves.

## General guidelines

* Follow the existing project structure and conventions.
* Prefer small, focused changes.
* Keep changes consistent with the project's existing tooling and configuration.
* Don't introduce unnecessary dependencies or complexity.
* Reuse existing functionality instead of unnecessarily creating new abstractions.
* Update tests and documentation when the change requires them.
* Don't modify unrelated parts of the project.
* Preserve existing public APIs unless the task explicitly requires a change.
* Avoid speculative changes or improvements outside the scope of the task.
* When unsure, inspect the existing code and project resources before making assumptions.

## Before making changes

Before implementing a change:

1. Understand the task and its intended scope.
2. Inspect the relevant source code, tests, configuration, and documentation.
3. Check applicable resources in `.agents/context/` and `.agents/skills/`.
4. Follow existing patterns unless there is a clear reason to change them.
5. Identify any affected tests, documentation, configuration, or public APIs.

## Before finishing

Before considering the task complete:

* Review the changes for unrelated modifications.
* Run the relevant tests and project checks when available.
* Verify that new or changed behavior is covered appropriately.
* Check formatting, linting, and type-checking when applicable.
* Update documentation when the change affects user-facing behavior or project usage.
* Keep the final changes focused on the original task.

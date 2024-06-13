Supporting files for use with Visual Studio Code.
Includes helper files for building tasks, recommended extensions, and support
for a dev container. See tools/docker for the dev container spec.

setup-vscode.sh will create links from the root of the project back to this folder.

- run setup-vscode.sh
- Launch VSCode
- If you wish to use a dev container,
  - install MS dev containers from Extensions (Ctrl-Shift-X), or
  - from the command palette (Ctrl-Shift-P): ext install ms-vscode-remote.remote-containers
  - no need to install additional extensions in the host
- From the Explorer (Ctrl-Shift-E), Open Folder: the base of this code repository
- Trust the authors (or not - untested)
- If you wish to use a dev container,
  - there should be a pop-up to "Reopen in Container" - do it!
  - If there is no pop-up, command palette (Ctrl-Shift-P): Dev Containers: Reopen in Container
- Install recommended extensions at this time (pop-up should automate), else:
  - ext install ms-vscode.cpptools
  - ext install llvm-vs-code-extensions.vscode-clangd
  - ext install augustocdias.tasks-shell-input
- Terminal -> Run Build Task (Ctrl-Shift-B): configure ardour
- Terminal -> Run Build Task (Ctrl-Shift-B): build ardour
- Run and Debug (Ctrl-Shift-D): Start Debugging (F5)

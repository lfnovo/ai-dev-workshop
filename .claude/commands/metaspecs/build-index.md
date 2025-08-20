
This is a documentation project for several open source projects for our organization. The idea for this repo is to be the one specification that drives all other specs, code, design and test artifacts. It is our canonical source of truth for all our projects.

Each project has its own folder under @/projects/ folder.
Inside each of these folders, there is an index.md file that points to all other useful resources in the project.

## Usage

### /build-index

If no arguments are provided, the command will build the root projects index.md file under the folder @/projects/
This index should provide basic information about each project, such as:

- name with link to its folder
- short description
- linear project id
- linear team id
- repository url

This information is easily available inside the projects main files (either index.md or 2-project_management.md)

Do not add anything else besides the information above.


### /build-index <project-name>

This is used to rebuild the project index after we change the directory and file structure.
Please go through the project's folder structure, understand what files and folders are there and refine the index.md file for the project. If the project doesn't have an index.md file, create it.  If it does, edit it to reflect the current structure.

The index should point to all other useful resources in the project folder.

Provided arguments: #$ARGUMENTS

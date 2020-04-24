# gitlab-ci-taskfiles
Import task files in GitlabCI w/h extends 

## Why
If you want to use task files in Gitlab CI, you are in for a surprise. 
- Yaml anchors are not processed over include statements
- Extends does not currently merge script blocks. This means you have to extend your task file to run as a before_ or after_ script or just have a complete script file in either your job in the pipeline or in your task. Also, before_, script, and after_script do run in different processes, so they do not share env.

## How
Using the preauth clone url, you can clone without setting up ssh or auth directly the task repository in a folder. From there, execute the files.

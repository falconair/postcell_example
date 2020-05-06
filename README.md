# postcell_example
Example project to demonstrate `postcell` functionality (see https://postcell.io for more info)


## Getting started: Students
1. Install `%%postcell` magic command via `pip install postcell`
2. If your instructor is using a configuration file, enter your name under `student_id` (the config file is most likely called `postcell.conf`, somewhere in the folder containing the notebook)
2. Do exercises in a notebook, provided to you by your instructor

Students don't need to register on any website.

## Getting started: Instructors

1. Register yourself as an instructor at http://postcell.io
2. Create a class (http://postcell.io/classes.html)
3. Click 'sample config' to get help in creating a configuration file (see "**How to configure notebooks**" below for alternatives)
4. Install the `%%postcell` magic command by running the following command `pip install postcell`

## How to configure notebooks
The following [link](https://github.com) provides a simple skeleton project.

Instructors will create a notebook with the following cells:

```
%reload_ext postcell
%postcell register 
```
This cell will load the `postcell` magic and register class name, instructor id and student id via a `postcell.conf` file (either in the same folder as the notebook or any of the parent folders).

Here is a sample config file:
```
{
"url" : "https://postcell.io/post_cell",
"student_id" : "TEST_STUDENT",
"instructor_id": "YOUR_INSTRUCTOR_ID",
"class_id": "IntroToPython",
"should_send_to_server" : true
}
```

Instructors can get their `instructor_id` and `class_id` from https://postcell.io/classes.html

`student_id` can be any arbitrary value, but instructors should have their students use a standard id, perhaps their email.

If a config file is too heavy weight (perhaps for a single notebook workshop), the following syntax can be used to bypass the need for a file:

```
%reload_ext postcell
%postcell register -student_id STUDENT_USER_NAME -url -instructor_id INSTRUCTOR_ID 
 -url https://postcell.io/post_cell 
```

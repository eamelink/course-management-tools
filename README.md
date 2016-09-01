# Lightbend Course *studentifier*

## Introduction

This application will generate a *student* repository based on a course master repository.

A student will clone a copy of the generated student repository, load it in his/her favorite IDE (IntelliJ or Eclipse).

Using either *sbt* or *activator*, the student can move between exercises by issuing the ```next``` or ```prev``` commands. 

Detailed, per-exercise instructions can be obtained via the ```man e``` command.

General course instructions can be obtained via the ```man``` command.

## Usage

### Requirements: 

* a master repository and its file-path
* the path to an (empty) folder in which the student distribution will be created

### Invocation:

```
studentify 1.0
Usage: studentify masterRepo out

  masterRepo  base folder holding master course repository
  out         base folder for student repo
```

### Example

```
studentify ./LightbendTraining/FTTAS-v1.3.0/fast-track-akka-scala ./LightbendTraining/Studentify/fttas-student
```

## Todo

* Leverage ```git```'s, ```.gitignore``` file to filter out file and folders that shouldn't end-up in student repository
* Implement ```front``` command
* Implement ```save``` and ```restore``` command that will allow a student to save/restore the state of an exercise for later investigation
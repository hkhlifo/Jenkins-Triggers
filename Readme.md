# Jenkins Pipeline README

## Overview

This project contains a simple Jenkins Declarative Pipeline script used for testing Jenkins pipeline stages and post-build actions.

The pipeline demonstrates:

* A basic `Build` stage
* Console output using `echo`
* Usage of `post` conditions:

  * `always`
  * `success`
  * `failure`

---

## Pipeline Structure

### Agent

```groovy
agent any
```

The pipeline can run on any available Jenkins agent.

---

## Stages

### Build Stage

The pipeline contains a single stage named:

```groovy
stage("Build")
```

Inside this stage, Jenkins prints the following message:

```groovy
echo "========executing Build========"
```

---

<!-- ## Post Actions

The pipeline includes post-execution actions for the `Build` stage. -->

### Always

Runs regardless of pipeline result.

```groovy
always {
    echo "========always========"
}
```

### Success

Runs only if the stage completes successfully.

```groovy
success {
    echo "========Build executed successfully========"
}
```

### Failure

Runs only if the stage fails.

```groovy
failure {
    echo "========Build execution failed========"
}
```

---

## Purpose

This pipeline is intended for:

* Jenkins testing
* Learning Declarative Pipeline syntax
* Understanding post conditions
* Verifying Jenkins setup

---

## Example Console Output

### Successful Build

```text
========executing Build========
========always========
========Build executed successfully========
```

### Failed Build

```text
========executing Build========
========always========
========Build execution failed========
```

---

## Requirements

* Jenkins installed
* Pipeline plugin enabled
* Access to create and run Jenkins jobs

---

## Usage

1. Create a new Pipeline Job in Jenkins
2. Paste the pipeline script into the Pipeline section
3. Save the job
4. Click **Build Now**
5. Check the Console Output

---

## File Example

```text
Jenkinsfile
README.md
```

---

## License

This project is for testing and educational purposes only.

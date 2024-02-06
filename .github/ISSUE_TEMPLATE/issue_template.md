name: New Deployment
description: Use this form to create a new deployment
labels: ["deployment"]
body:
  - type: markdown
    attributes:
      value: |
        ## Instructions
        instructions go here

  - type: input
    id: input1
    attributes:
      label: Text Field 1
      placeholder: Type something..
    validations:
      required: false

  - type: input
    id: input2
    attributes:
      label: Text Field 2
      placeholder: Type something..
    validations:
      required: false

  - type: input
    id: input3
    attributes:
      label: Text Field 3
      placeholder: Type something..
    validations:
      required: false

  - type: checkboxes
    id: Releases
    attributes:
      label: Releases
      description: Select all the releases to include in this deployment
      options:
        - label: release 5
        - label: release 4
        - label: release 3
        - label: release 2
        - label: release 1
    validations:
      required: true

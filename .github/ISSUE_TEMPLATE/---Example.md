name: "🐞 Bug Report2"
description: "Report a reproducible bug in the project"
labels: 🐞 Bug
body:
- type: markdown
  attributes:
  value: |
  Thanks for taking the time to file a bug report! Before filling out a new issue, please first check to see if your question has been answered in an existing issue, or in the project documentation at [https://example.com](https://example.com)

      **Please note** The project is supported for free on a voluntary basis. If you use the project please [sponsor the project](https://github.com/sponsors/MrVitaly) so that its development can continue. Bug reports from sponsors will be prioritised.
      
      Please take the time to fill in this form as completely as possible. If you leave out sections there is a high likelihood your issue will be closed.

-- type: input
id: prevalence
attributes:
label: Bug prevalence
description: "How often do you or others encounter this bug?"
placeholder: "Whenever I visit the user account page (1-2 times a week)"
validations:
required: true

- type: textarea
  id: repro
  attributes:
  label: Reproduction steps
  description: "How do you trigger this bug? Please walk us through it step by step."
  value: |
  1.
  2.
  3.
  ...
  render: bash
  validations:
  required: true

- type: dropdown
  id: download
  attributes:
  label: How did you download the software?
  description: Some description
  multiple: true
  options:
  - Homebrew
  - MacPorts
  - apt-get
  - Built from source
  validations:
  required: true

- type: checkboxes
  id: cat-preferences
  attributes:
  label: What kinds of cats do you like?
  description: You may select more than one.
  options:
  - label: Orange cat (required. Everyone likes orange cats.)
  required: true
  - label: **Black cat**

name: Bug Report
description: File a new bug report.
body:
- type: textarea
  id: logs
  attributes:
  label: Log output
  description: What do you see when you run `cat ./logs/*.log` from the project directory?
  render: shell
- type: textarea
  id: config
  attributes:
  label: YAML Configuration
  description: Please include the workflow configuration YAML snippet
  render: yaml
  
- type: markdown
  attributes:
  value: |
  Please ensure that any code samples are readable and [properly formatted as code blocks](https://docs.github.com/en/github/writing-on-github/creating-and-highlighting-code-blocks).

      **Please realise that it is up to you to debug your code thorougly. Be as certain as possible that the bug is with the project, and not with your own code, prior to opening an issue.**

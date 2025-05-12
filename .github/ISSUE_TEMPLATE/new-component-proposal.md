---
name: New Component Proposal
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

name: New component
description: Create a new component in Polaris
title: "[New component]: "
labels: ["Type: Enhancement :sparkles:", "Status: Proposal :thought_balloon:"]
assignees: []
body:
  - type: markdown
    attributes:
      value: |
        # New component proposal

        Thanks for taking the time to propose a new component!
        
        This template will help you think through what's needed to make a successful component proposal.
  - type: input
    id: component_name
    attributes:
      label: Component name
      description: What is the name of your proposed component?
      placeholder: Button
    validations:
      required: true
  - type: textarea
    id: description
    attributes:
      label: Description
      description: Provide a brief, clear description of what this component is and what it does.
      placeholder: A button is a clickable element used to trigger an action or event.
    validations:
      required: true
  - type: textarea
    id: use_cases
    attributes:
      label: Use cases
      description: What are the main use cases for this component? When and why would merchants use it?
      placeholder: |
        - Submit forms
        - Trigger actions like "Save", "Delete", etc.
        - Navigate between pages or sections
    validations:
      required: true
  - type: textarea
    id: designs
    attributes:
      label: Designs
      description: |
        Please share any designs, mockups, or examples of the component. You can upload images directly or link to Figma files.
        
        If you don't have designs yet, describe how you envision the component looking.
      placeholder: |
        [Figma link] or [Description of visual appearance]
    validations:
      required: false
  - type: textarea
    id: composition
    attributes:
      label: Composition
      description: |
        How do you envision this component being composed?
        
        Does it use existing Polaris components? Does it need to be broken down into smaller components?
      placeholder: |
        This component would use the existing Text component for labels and could be composed with Icon for button icons.
    validations:
      required: false
  - type: textarea
    id: behavior
    attributes:
      label: Behavior
      description: |
        Describe how the component should behave. Include any interactions, states, animations, etc.
      placeholder: |
        The button should have hover, focus, active, and disabled states. When clicked, it should trigger the specified action.
    validations:
      required: true
  - type: textarea
    id: accessibility
    attributes:
      label: Accessibility considerations
      description: |
        What accessibility requirements should this component fulfill? 
        
        Consider keyboard navigation, screen readers, color contrast, etc.
      placeholder: |
        - Should be keyboard accessible
        - Need proper ARIA attributes
        - Must have sufficient color contrast
        - Should work with screen readers
    validations:
      required: true
  - type: textarea
    id: api_proposal
    attributes:
      label: Proposed API
      description: |
        What props, slots, or other API features do you envision for this component?
      placeholder: |
        ```tsx
        <Button
          primary={boolean}
          destructive={boolean}
          size="small" | "medium" | "large"
          icon={<Icon />}
          fullWidth={boolean}
          disabled={boolean}
          loading={boolean}
          onClick={() => {}}
        >
          Button text
        </Button>
        ```
    validations:
      required: false
  - type: textarea
    id: similar_components
    attributes:
      label: Similar components
      description: |
        Are there similar components in Polaris already? If so, why is a new component needed? 
        
        Are there similar components in other design systems we could learn from?
      placeholder: |
        This is similar to the existing Button component but differs in [specific ways].
        
        Material Design and Ant Design have similar components that handle [specific features] in [specific ways].
    validations:
      required: false
  - type: textarea
    id: alternatives
    attributes:
      label: Alternatives considered
      description: |
        What alternatives have you considered? Why is this proposal better?
      placeholder: |
        I considered extending the existing Button component, but that would add too much complexity to its API.
    validations:
      required: false
  - type: textarea
    id: additional_context
    attributes:
      label: Additional context
      description: |
        Add any other context or information about the proposed component here.
      placeholder: |
        This component request is related to issue #123.
    validations:
      required: false
  - type: checkboxes
    id: terms
    attributes:
      label: Code of Conduct
      description: By submitting this proposal, you agree to follow our [Code of Conduct](https://github.com/Shopify/polaris/blob/main/CODE_OF_CONDUCT.md)
      options:
        - label: I agree to follow Shopify's Code of Conduct
          required: true

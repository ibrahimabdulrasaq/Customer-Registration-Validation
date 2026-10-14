# Customer Registration Validation Workflow

## Project Overview

This project demonstrates a simple workflow automation built with n8n to validate customer registration form submissions.

The workflow checks whether a customer has provided their name and directs the submission to the appropriate response based on the result.

This project was developed as part of my AI automation learning journey to practise applying workflow automation concepts to practical business scenarios.

## Business Problem

When businesses collect customer registrations through online forms, they need a way to identify submissions where required information is missing.

Manually checking every submission can become time-consuming, especially when dealing with multiple registrations.

This workflow demonstrates how conditional logic can automate a basic validation process and provide an appropriate response to the customer.

## Project Objective

To build an automated workflow that checks whether a customer's name has been provided and directs the submission to the appropriate outcome.

## Tools Used

- **n8n:** Workflow automation.
- **Form Trigger:** Captures customer registration submissions.
- **Edit Fields:** Prepares the submitted data for subsequent processing.
- **IF Node:** Evaluates the submitted name against a condition.
- **Form Ending:** Provides the appropriate response based on the condition.

## Workflow Architecture

The workflow follows this sequence:

```text
Customer Submits Form
         |
         v
     Edit Fields
         |
         v
      IF Node
         |
         |---------------------|
         |                     |
       TRUE                  FALSE
         |                     |
         v                     v
Registration Success      Error Response
```

## Workflow Overview

<img width="1323" height="511" alt="Screenshot 2026-10-14 140524" src="https://github.com/user-attachments/assets/65df60fc-1f34-471a-bc8f-f647b1603066" />

<img width="1322" height="510" alt="Screenshot 2026-10-14 140627" src="https://github.com/user-attachments/assets/181703b4-ac16-46d6-ae7e-d7e17a9eb9f9" />

## How It Works

**Step 1: Form Submission**

The workflow starts when a customer submits the registration form.

**Step 2: Edit Fields**

The Edit Fields node prepares the submitted information for evaluation.

**Step 3: Conditional Validation**

The IF node checks whether the customer has provided their name.

**Step 4: Route the Submission**

The workflow follows one of two paths:

- **True:** If the name meets the configured condition, the submission proceeds to the successful registration response.
- **False:** If the name does not meet the condition, the submission proceeds to the error response.

**Step 5: Return a Response**

The appropriate form-ending node provides feedback based on the result of the validation.

## Expected Outcome

The workflow demonstrates how a simple registration validation process can be automated using conditional logic.

## Key Learning Outcomes

Through this project, I practised:

- Building a workflow in n8n.
- Connecting workflow nodes.
- Using conditional logic to evaluate submitted data.
- Routing submissions based on evaluation results.
- Applying automation to a practical business scenario.

## Future Improvements

Potential enhancements include:

- Storing valid registrations in Google Sheets or a database.
- Sending email confirmations to customers.
- Validating additional required fields.
- Detecting names containing only whitespace.
- Recording invalid submissions for review.

## Acknowledgement

Huge thanks to my facilitator, [Ebuka Analugwo](https://www.linkedin.com/in/ebuka-anulugwo), whose teaching and guidance played a key role in making this possible, and to The Incubator Hub for providing this opportunity.

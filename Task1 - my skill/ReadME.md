# AI Skill Creation – Bug Report Generator

## Project Overview

As a Software Test Engineer, one of my daily responsibilities is creating bug reports. Writing detailed and well-structured bug reports is often time-consuming and requires careful thinking to ensure all necessary information is included.

To improve my productivity and maintain consistency across bug reports, I used Claude to create a reusable AI skill that automatically generates a standardized bug report template.

---

## AI Tool Used

- Claude AI

---

## Objective

Create a reusable AI skill that generates a bug report template with all the required sections in the correct order, making bug reporting faster, more consistent, and easier to complete.

---

## Prompt Given to Claude to create a skill

```text
/skill-creator

Create a Bug Report format.

The bug report should contain the following headings in this exact order:

1. Environment
2. Description
3. Logs or Screenshot
4. Steps to Reproduce
5. Expected Result
6. Actual Result
```

---

## Generated Bug Report Template

```markdown
# Bug Report

## Environment
- Application:
- Version:
- Browser/Device:
- Operating System:
- Test Environment:

## Description
Provide a clear description of the issue.

## Logs or Screenshot
Attach relevant logs, screenshots, or videos.

## Steps to Reproduce
1.
2.
3.

## Expected Result
Describe the expected behavior.

## Actual Result
Describe the actual behavior observed.
```

---

## Benefits

- Saves time during bug reporting.
- Ensures consistency across all bug reports.
- Reduces the chances of missing important information.
- Makes bug reports easier for developers to understand and reproduce.
- Improves overall testing efficiency.

---

## Outcome

By creating this AI skill, I can quickly generate a professional bug report template whenever needed. Instead of manually remembering the report structure, 
I can focus more on testing and accurately describing the issue.

# Testing
This prompt given for testing
<img width="1004" height="620" alt="image" src="https://github.com/user-attachments/assets/7170931f-02c8-4d08-98c5-9c834a80eca4" />

and it verified that skill is used 
<img width="1004" height="544" alt="image" src="https://github.com/user-attachments/assets/5f782e5a-1284-42d9-a305-7e028178b978" />



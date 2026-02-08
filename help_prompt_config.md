# Prompt Configuration

This guide will help you get started with creating and configuring prompts that generate formatted text. The interface is designed to be intuitive and user-friendly, allowing you to define templates and input parameters with ease.

## Overview

The Prompt Configuration interface enables you to create reusable templates for generating formatted text. Each prompt has a name, description, template, and a set of arguments that define the input requirements. The system supports both optional and required arguments, with input masks to validate user input.

## Getting Started

### 1. Create a New Prompt

To begin, click the "Add Prompt" button to create a new prompt configuration. This will open a new configuration window where you can define your prompt.

### 2. Enter the Name

Provide a name for your prompt. This name will be used to identify your prompt in the list of available prompts. For example, you might name your prompt "Text Generator".

### 3. Add a Description

Write a brief description of what the prompt generates. This description will help users understand the purpose of the prompt. For example, "Generates formatted text".

### 4. Define the Template

Enter the template string that defines the output format. Use placeholders to specify where user input should be inserted. For example:
```
Create a text about {topic} in style {style}
```
In this example, `{topic}` and `{style}` are placeholders that will be replaced with user input.

### 5. Configure Arguments

Add arguments to your prompt and specify whether they are optional or required.

- **Optional**: The argument can be left blank.
- **Required**: The argument must be provided.

For example, you might have two arguments:
- **style**: Optional
- **topic**: Required

### 6. Save the Configuration

Click the "Save" button to save your prompt configuration. Your prompt is now ready to use.

## Best Practices

- **Use Clear Placeholders**: Use descriptive names for placeholders in the template to make it easier for users to understand what to input.
- **Validate Input**: Use input masks to ensure that users provide valid input for each argument.
- **Test Your Prompts**: Test your prompts with different inputs to ensure they generate the expected output.

By following these steps, you can create effective and user-friendly prompt configurations. Get started today and begin generating formatted text with ease!

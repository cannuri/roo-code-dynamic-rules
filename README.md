# Roo Code Dynamic Rules

This repository provides a streamlined way to dynamically update your project's rules as you work. Simply configure the `.clinerules` file in your project’s root directory to allow Roo Code to learn and adapt its behavior based on user interactions.

## How It Works

When you need to modify Roo Code’s behavior, just prepend your instruction with `RULE:`. Roo Code automatically appends these directives to the `.clinerules` file under the **Additional Rules** section. This ensures that your project-specific rules are consistently maintained throughout the project lifecycle.

If you want to delete a rule simply use "NORULE: " followed by the rule you want to be forgotten.

## .clinerules Configuration

Copy or add the following snippet to your project's `.clinerules` file:

```
## Additional Rules

- When a user requests additional rules, add them to the "Additional Rules" section of the `.clinerules` file in the project's root directory.
- Identify new rules by the prefix `RULE:` in user messages.
- For example, if the user writes `RULE: keep the README.md up to date`, append the rule as `- keep README.md up to date`.
- In contrary if a user write `NORULE:` you remove the according line from the "Additional Rules" section.
- Persist these rules throughout the project lifecycle.
- Ensure that all added rules are clear, specific, and actionable.
- Format each rule as a separate bullet point.
```

Now, whenever you want Roo Code to remember a new rule, simply type:
```
RULE: run all tests at the end of a task
```
or let it forget the rule by:
```
NORULE: run all tests at the end of a task
```

Roo Code will then update your `.clinerules` file accordingly and add `- Run all Tests at the end of a task` to it and also follow this new rule.

## License

This project is open source and available under the MIT License.
```

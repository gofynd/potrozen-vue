# Nitrozen Custom Form

```
name: 'nitrozen-custom-form',
props:
    inputs: Array of Inputs
    value: Object (Form Response v-model)
```

---

Example of an Input

```
{
    type: "toggle",
    display: "Does your file have a header?",
    key: "fileHasHeader",
    default: false,
}
```

Response for a form containing only this input would be
```
{
    fileHasHeader: false
}
```

---


Possible Values of `type`:

```
{
    text: {
        display: "Single line input",
        description: "Single line of text"
    },
    textarea: {
        display: "Multi line input",
        description: "Multiple lines of text"
    },
    mobile: {
        display: "Mobile Number",
        description: "Input field for Country code and Mobile number"
    },
    email: {
        display: "Email",
        description: "Email ID"
    },
    number: {
        display: "Numeric input",
        description: "Numeric input."
    },
    radio: {
        display: "Radio Button Group",
        description: "Multiple choice question, single answer."
    },
    checkbox: {
        display: "Chexbox Group",
        description: "Multiple choice question, multiple answers."
    },
    dropdown: {
        display: "Dropdown",
        description: "Multiple choice dropdown."
    },
    toggle: {
        display: "Toggle",
        description: "An on-off toggle switch."
    },
    object: {
        display: "Group of Inputs",
        description: "Group of inputs which will be responsed in sub key"
    },
    array: {
        display: "Input having array as response",
        description: "Input having array as response"
    },
}
```


`key` from input will be used to store data in response and is compulsory for all inputs.

`enum` key is needed for `dropdown`, `checkbox`and `radio` type of inputs.

`disabled`, `required`, `hidden` and `default` are the other common options supported in all inputs.

`min` and `max` are supported for `number` type of inputs.

`min_length` and `max_length` are supported for `text`, `textarea` and `email` type of inputs.

`regex` is supported for `text` and `textarea` type of inputs.

`tooltip` is supported for almost all kind of inputs.

`visible_if` is supported for all inputs and [json-logic-js](https://www.npmjs.com/package/json-logic-js) is used for this.

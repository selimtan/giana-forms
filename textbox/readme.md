# Textbox
The TextBox is a control that enables a user to enter and edit a single line of text.

```json
 {
    "type": "textbox",
    "key": "",
    "label": "",
    "label$":"",
    "hint":"",
    "hint$":"",
    "mask":"",
    "mask$":"",
    "placeholder":"",
    "placeholder$":"",
    "disabled":false,
    "disabled$":"",
    "visible":true,
    "visible$":"",
    "required": false,
    "required$": "",
    "readonly":false,
    "readonly$":"",
    "autocomplete": false,
    "spellcheck": false,    
    "maxlength": 70,
    "tabindex": 0,
    "validationError":"",
    "validationError$":"",
    "order": 1
}
```

### type
Type of control. In this case it is textbox.

### key
Data key for this control.

### label
Specifies text for a label that this control.

### label$
Expression for label text. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).   

### hint
Specifies text for a hint that appears when a user pauses on the control.

### hint$
Expression for hint text. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).

### mask
The editor mask that specifies the format of the entered string.

Masking Element  | Description
:---:       | ---
0| A digit.
9| A digit or a space.
#| A digit, a space, "+" or "-" sing.
L| A literal.
C| Any character except space.
c| Any character.
A| An alphanumeric.
a| An alphanumeric or a space.

```
To escape the masking elements, use the double backslash character (\). 
For example, "000.\\0\\0".
```

### mask$
Expression for mask text. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).

### placeholder
The text displayed by the control when the control value is empty.

### placeholder$
Expression for placeholder text. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).

### disabled
Specifies whether the control responds to user interaction.

### disabled$
Expression for disabled property. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).

### visible
Specifies whether the control is visible.

### visible$
Expression for visible property. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).

### required
Specifies whether the control value must enter.

### required$
Expression for required property. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).

### readonly
A Boolean value specifying whether or not the control is read-only.

### readonly$
Expression for readonly property. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).

### autocomplete
---

### spellcheck
---

### maxlength
Specifies the maximum number of characters you can enter into the textbox.

### tabindex
Specifies the number of the element when the Tab key is used for navigating.

### validationError
Holds the message that defines the error that occurred during validation.

### validationError$
Expression for validationError property. See more detail to [expressions](https://github.com/selimtan/gianaForms/tree/master/expressions.md).

### order
Replacement order of the control in the form.
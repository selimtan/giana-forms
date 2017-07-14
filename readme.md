# Giana Forms
Giana forms contains json based spesifications for generating automatic forms.
Bu spesifikasyonun temel amacı ortak bir form tanımlama standartı oluşturup tüm platformlarda bu spesifikasyonu destekleyen kütüphaneler sayesinde form tasarlamayı ve oluşturma işini platform bağızsız hale getirmektir.
Temel özellikleri;

⋅⋅* Unordered sub-list. 


This form spesification contains following controls spesifications;

Property  | Description
---       | ---
[Textbox](https://github.com/selimtan/gianaForms/tree/master/textbox)           | Textbox control spesification for giana forms
[Button](https://github.com/selimtan/gianaForms/tree/master/button)     | Button control spesification for giana forms
[Calendar](https://github.com/selimtan/gianaForms/tree/master/calendar)         | Calendar control spesification for giana forms
[Title](https://github.com/selimtan/gianaForms/tree/master/title)         | Title control spesification for giana forms
[datepicker](https://github.com/angular/angular-cli/wiki/generate-interface) | Datepicker control spesification for giana forms
[texteditor](https://github.com/angular/angular-cli/wiki/generate-enum)           | Texteditor control spesification for giana forms
[dropdown](https://github.com/angular/angular-cli/wiki/generate-module)       | Dropdown control spesification for giana forms


## Installation

**BEFORE YOU INSTALL:** please read the [prerequisites](#prerequisites)
```bash
npm install giana-forms-spec
```


## Simple Form Sample


```json
 {
   "type": "textbox",
    "key": "",
    "label": "",
    "required": false,
    "autocomplete": false,
    "spellcheck": false,
    "maxlength": 70,
    "tabindex": 0,
    "order": 1
}
```
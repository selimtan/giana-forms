
# DataSource
The Datasource is a component of giana form that include queries.

```json
{
      "type": "datasource",
      "key": "users",
      "url": "http://localhost:3002/db/get/users",
      "queries": [
        {
          "name": "currentData",
          "query$": "users.select('UserID',params.UserID)"
        }
      ]
    }
```

### type
Type of control. In this case it is calendar.

### key
Unique key for this component.

### url
Json result data url.

### queries
Collection of the query object definition.

## Example 

```json
{
  "key": "userDetailForm",
  "title": "",
  "screenMode": "half",
  "postUrl": "http://localhost:3002/db/save/users",
  "controls": [
    {
      "type": "datasource",
      "key": "users",
      "url": "http://localhost:3002/db/get/users",
      "queries": [
        {
          "name": "currentData",
          "query$": "users.select('UserID',params.UserID)"
        }
      ]
    },
     {
      "type": "popup",
      "key": "selectParentLocation",
      "formUrl": "http://localhost:3002/forms/locations/locations.gf.json",
      "value$":"users.currentData.UserLocation"
    },
     {
      "type": "popup",
      "key": "selectExpenceCenter",
      "formUrl": "http://localhost:3002/forms/expenceCenter/expenceCenters.gf.json",
      "value$":"users.currentData.UserExpenceCenter"
    },
    {
      "type": "uuid",
      "key": "UserID",
      "value$": "params.UserID === undefined ? undefined : users.currentData.UserID",
      "order": 0
    },
    {
      "type": "title",
      "key": "lbTitle",
      "title": "Kullanıcı Ekle",
      "title$": "currentData === undefined ? 'Yeni Kullanıcı Ekle' : currentData.UserName + ' ' + currentData.UserSurname",
      "subtitle": "Lütfen istediğiniz değişiklikleri yaptıktan sonra [Kaydet] butonuna basın",
      "required": false,
      "order": 1
    },
    {
      "type": "textbox",
      "key": "UserEmployeNo",
      "label": "Sicil No",
      "value$": "users.currentData.UserEmployeNo",
      "required": false,
      "autocomplete": false,
      "spellcheck": false,
      "maxlength": 70,
      "tabindex": 0,
      "order": 1
    },
    {
      "type": "textbox",
      "key": "UserName",
      "label": "Adı",
      "value$": "users.currentData.UserName",
      "required": false,
      "autocomplete": false,
      "spellcheck": false,
      "maxlength": 70,
      "tabindex": 0,
      "order": 1
    },
    {
      "type": "textbox",
      "key": "UserSurname",
      "label": "Soyadı",
      "value$": "users.currentData.UserSurname",
      "required": false,
      "autocomplete": false,
      "spellcheck": false,
      "maxlength": 70,
      "tabindex": 1,
      "order": 1
    },
    {
      "type": "textbox",
      "key": "UserEmail",
      "label": "Email",
      "value$": "users.currentData.UserEmail",
      "required": false,
      "autocomplete": false,
      "spellcheck": false,
      "maxlength": 70,
      "tabindex": 2,
      "order": 1
    },
      {
      "type": "texteditor",
      "key": "UserLocation",
      "label": "İşyeri",
      "value$": "selectParentLocation.value",
      "textField$": "'#' + selectParentLocation.value.LocationName",
      "required": false,
      "autocomplete": false,
      "spellcheck": false,
      "maxlength": 70,
      "tabindex": 2,
      "order": 1,
      "buttons": [
        {
          "buttonName": "selectUser",
          "buttonIcon": "user",
          "click$": ["selectParentLocation.showModal()"]
        }
      ]
    },
     {
      "type": "texteditor",
      "key": "UserExpenceCenter",
      "label": "Masraf Yeri",
      "value$": "selectExpenceCenter.value",
      "textField$": "'#' + selectExpenceCenter.value.ExpenceCenterName",
      "required": false,
      "autocomplete": false,
      "spellcheck": false,
      "maxlength": 70,
      "tabindex": 2,
      "order": 1,
      "buttons": [
        {
          "buttonName": "selectUser",
          "buttonIcon": "user",
          "click$": ["selectExpenceCenter.showModal()"]
        }
      ]
    },
    {
      "type": "dropdown",
      "key": "UserCategory",
      "label": "Kategori",
      "labelKey": "label",
      "valueKey": "value",
      "value$":"users.currentData.UserCategory",
      "options": [
        {
          "label": "Kapsam İçi",
          "value": "Kapsam İçi"
        },
        {
          "label": "Kapsam Dışı",
          "value": "Kapsam Dışı"
        }
      ],
      "required": false,
      "order": 3
    },
     {
      "type": "date",
      "key": "UserBornDate",
      "value$":"users.currentData.UserBornDate",
      "label": "Doğum Tarihi",
      "required": false,
      "order": 3
    },
     {
      "type": "date",
      "key": "UserWorkDate",
      "value$":"users.currentData.UserWorkDate",
      "label": "İşe Giriş Tarihi",
      "required": false,
      "order": 3
    }
  ]
}
```
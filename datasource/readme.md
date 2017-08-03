
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
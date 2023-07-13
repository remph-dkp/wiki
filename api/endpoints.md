# API Endpoints

All API calls send POST requests, and all responses use a JSON payload. 

The POST request must contain the following fields

```
{
  'service': 'remph',
  'key': (API KEY),
  'secret': (API SECRET),
  // action-specific fields
}
```

### Character

#### Create a Character

Creates a new character in the system.

Endpoint: `/api/character`

Content:
```
'action': 'character create',  // required
'name': (character name, case-sensitive),  // required, name of the character
'roles': [(role ID 1), (role ID 2), ...],  // optional, roles to assign the character
'stats': {  // optional, stats to assign the character
            (stat ID 1) : (stat value),
            (stat ID 2) : (stat value),
            ...
         }
```

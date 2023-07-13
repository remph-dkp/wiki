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

### Community

#### Create a Community

Create a new community in the community.

Endpoint: `/api/community`

Content:
```
'action': 'community create',  // required
'name': (community name, case-sensitive),  // required, name of the community
'template': (template ID)  // optional, template to base the community on
```

#### Add a Role

Add a role to a community if it doesn't already exist on the community.

Endpoint: `/api/community`

Content:
```
'action': 'community role add',  // required
'community': (community id),  // required, ID of the community
'roles': [(role ID 1), (role ID 2), ...]  // required, roles to add to the community
```

#### Remove a Role

Remove a role from a community.

Endpoint: `/api/community`

Content:
```
'action': 'community role remove',  // required
'community': (community id),  // required, ID of the community
'roles': [(role ID 1), (role ID 2), ...]  // required, roles to remove from the community
```

#### Update a Stat

Add a stat to a community, or update the stat if it already exists on the community.

Endpoint: `/api/community`

Content:
```
'action': 'community stat add',  // required
'community': (community id),  // required, ID of the community
'stats': [(stat name 1), (stat name 2), ...]  // required, stat names to add to the community
```

#### Remove a Stat

Removes a stat from a community

Endpoint: `/api/community`

Content:
```
'action': 'community role remove',  // required
'community': (community id),  // required, ID of the community
'stats': [(stat ID 1), (stat ID 2), ...]  // required, stats to remove
```

#### Update Community Name

Update a community's name

Endpoint: `/api/community`

Content:
```
'action': 'community name update',  // required
'community': (community id),  // required, ID of the community
'name': (new community name),  // required, new name of the community
```

### Character

#### Create a Character

Create a new character in the community.

Endpoint: `/api/character`

Content:
```
'action': 'character create',  // required
'community': (community ID),  // required
'name': (character name, case-sensitive),  // required, name of the character
'member': (member ID),  // required, member to assign the character to
'roles': [(role ID 1), (role ID 2), ...],  // optional, roles to assign the character
'stats': {  // optional, stats to assign the character
            (stat ID 1) : (stat value),
            (stat ID 2) : (stat value),
            ...
         }
```

#### Add a Role

Add a role to a character if it doesn't already exist on the character.

Endpoint: `/api/character`

Content:
```
'action': 'character role add',  // required
'community': (community ID),  // required
'character': (character id),  // required, ID of the character
'roles': [(role ID 1), (role ID 2), ...]  // required, roles to assign the character
```

#### Remove a Role

Remove a role from a character.

Endpoint: `/api/character`

Content:
```
'action': 'character role remove',  // required
'community': (community ID),  // required
'character': (character id),  // required, ID of the character
'roles': [(role ID 1), (role ID 2), ...]  // required, roles to remove from the character
```

#### Update a Stat

Add a stat to a character, or update the stat if it already exists on the character.

Endpoint: `/api/character`

Content:
```
'action': 'character stat add',  // required
'community': (community ID),  // required
'character': (character id),  // required, ID of the character
'stats': {  // required, stats to assign the character
            (stat ID 1) : (stat value),
            (stat ID 2) : (stat value),
            ...
         }
```

#### Remove a Stat

Removes a stat from a character

Endpoint: `/api/character`

Content:
```
'action': 'character role remove',  // required
'community': (community ID),  // required
'character': (character id),  // required, ID of the character
'stats': [(stat ID 1), (stat ID 2), ...]  // required, stats to remove
```

#### Update Character Name

Update a character's name

Endpoint: `/api/character`

Content:
```
'action': 'character name update',  // required
'community': (community ID),  // required
'character': (character id),  // required, ID of the character
'name': (new character name),  // required, new name of the character
```

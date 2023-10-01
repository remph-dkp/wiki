# Kill

A Kill is a boss kill. Kills generally award points and can drop items that players can claim.

### Properties
* ID (`int`) : generated automatically and used to reference the kill
* Boss (`Boss`)
* Drops (`Drop` list)
* Attendance (`Character` list)
* Transactor (`Member`) : the player who generated the kill

### Functions
* Set the boss
* Set the value towards a system
* Add/remove attendees
* Add/remove drops
* Delete the kill

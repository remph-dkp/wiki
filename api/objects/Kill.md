# Kill

A Kill is a boss kill. Kills generally award points and can drop items that players can claim.

### Properties
* Boss (`Boss`)
* ID (`int`) : generated automatically and used to reference the kill
* Drops (`Drop` list)
* Attendance (`Character` list)
* Value (`System` to `int` map)
* Creator (`Member`)

### Functions
* Set the boss
* Set the value towards a system
* Add/remove attendees
* Add/remove drops

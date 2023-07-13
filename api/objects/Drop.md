# Drop

A Drop is an instance of an item gained from a kill. Drops are claimed by and awarded to players.

### Properties
* Kill (`Kill`) : reference to the kill the drop came from
* Item (`Item`) : reference to the item template
* System (`Systems) : reference to the point system this drop belongs to
* Claims (`Claim` list) : reference to all claimants, pulled from the System's Claim Ledger
* Transactor (`Member`) : the player who created this drop

### Functions
* Set the kill
* Set the item
* Set the system

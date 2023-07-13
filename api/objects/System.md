# System

A System is a point system. This is the core data structure that visualizations and information display pull from. A Point System is effectively a set of ledgers.

### Properties
* Name (`string`)
* Description (`string`)
* Transaction Ledger (`Transaction` list)
* Claim Ledger (`Claim` list)
* Kill Ledger (`Kill` list)
* Permissions (`Title` to `int` map)

### Functions
* Set the System name, description
* Set Title permissions
* Add/edit/remove a Transaction
* Add/edit/remove a Claim
* Add/edit/remove a Kill

### Title Permissions
* Create transactions
* Modify transactions
* Delete transactions
* Create claims
* Modify claims
* Delete claims
* Create kills
* Modify kills
* Delete kills

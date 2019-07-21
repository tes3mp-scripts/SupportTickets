A system to collect bug reports and feedback from players direclty on the game server.

Requires [DataManager](https://github.com/tes3mp-scripts/DataManager) and [GuiFramework](https://github.com/tes3mp-scripts/GuiFramework)!

Adds commands `/ticket` and `/tickets` that allow to create a new report ticket or few a list of the respecitvely.

A `teleportActions.lua` module is included, which will allow admins to teleport to location in which a ticket was made, or to its author. To enable it, require it in `customScripts.lua` by adding a `require("custom.SupportTickets.teleportActions")` line.

Keep in mind that for any such modules to work, SupportTickets itself should be assigned to a global variable with the same name.

Configuration
=====
* `ticketManagementRank` minimal rank that is allowed to view other players' tickets and manage them. Moderator (`1`) by default.  
* `ticketsPerPage` amount of tickets shown per page. By default `11`.  
* `saveDateString` whether data strings should be cached. Set it to false if you expect to change the data format in the future. `True` by default.  
* `dateFormat` format in which dates are displayed. Does not affect sorting. Default formt is `%y/%m/%d %H:%M"`

Commands
====
* `/ticket` asks the player for a ticket's title and detailed descriptions and saves them.
* `/tickets` when used by a player, shows them their own tickets. When used by an admin, shows all open tickets.
* `/tickets <playerName>` only available to admins, shows them list of all tickets made by player with name `<playerName>`.

All ticket lists are sorted in descending order, so newest tickets appear first. You can simply go to the last page if you wish to see the earliest tickets first.

Custom admin actions
====
Add new buttons to the admin ticket menu by using the `registerAdminAction(buttonLabel, callback)` function. You can find an example in `teleportActions.lua`.
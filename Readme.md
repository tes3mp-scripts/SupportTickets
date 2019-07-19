A system to collect bug reports and feedback from players direclty on the game server.

Adds commands `/ticket` and `/tickets` that allow to create a new report ticket or few a list of the respecitvely.

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
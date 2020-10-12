# gbf-api
granblue api

Building an API to be hosted which allows the grabbing of character data from the game Granblue Fantasy.  The API will be served through a Node.js server with a MongoDB backend.  Data is currently being filled through  Python web crawler on GBF.wiki to gather and parse character information. An admin panel created in React.js will also be available on the server to allow adding information to the database or fixing any discrepancies with the crawler (ie special buffs, etc).

The current plan is to have this information available for characters only so that it can be used to assist with hunting for party setups.  There are already tools out there to handle weapon damage calculation and grids, but as this API is being built generally that information can be added as a separate table.

Current functionality:

/char/{ID}
Get the character with their unique ID.

/char?name={NAME}
Get a list of characters whose name contains NAME.

/char?buffs=BUFF1,BUFF2,BUFF3,BUFF4...
Get a list of characters whose ougi or skills provide BUFF1 and BUFF2 and BUFF3...

/char?uncap={NUM}
Get a list of characters who have a max uncap of NUM.

/char?element={EL}
Get a list of characters whose main element is EL.

/char?specialty=SP1,SP2...
Get a list of characters who have weapon proficiencies SP1 and SP2...

/char?type=TYPE
Get a list of characters who are listed as a certain character type (Attack, Defense, Balanced, Special, Healer)

/char?race=RACE1,RACE2....
Get a list of characters who are listed as a certain character race (Human, Unknown, Harvin, Erune, Draph)

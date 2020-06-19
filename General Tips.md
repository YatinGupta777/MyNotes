
Didnt test API properly
Removes user when a new ticket book

Doesnt differentiate between create and update API.
using update api and a new booking is made on a cancelled seat. Calling createAPI first, then if false calling UpdateAPI then.

Too many ifs and checking. complexitiy increase
Dont use var
Dont set env variables.
Always read it


Api should be consistent. /create/ticket and rest are /ticket/open etc.


show open tickets implemented in a way which always show tickets when they are booked at least once.


Can make a /start api to start a system

Never depend on validation on frontend
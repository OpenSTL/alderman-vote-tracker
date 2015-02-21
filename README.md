# alderman-vote-tracker
Board of Alderman Vote Tracker for City of St. Louis

This project began at #CodeAcross 2015 and details are on the #CodeAcross wiki here: [https://github.com/OpenDataSTL/codeacross2015/wiki/Board-of-Alderman-Vote-Tracker](https://github.com/OpenDataSTL/codeacross2015/wiki/Board-of-Alderman-Vote-Tracker)

Right now, big focus is on liberating the vote data from City Journal PDFs - these should be saved as .csv files in /data/.

Below is a proposed format for tracking the vote data.  It is very possible additional fields will need to be tracked - if you start digging into the City Journals and realize this format is not sufficient, please suggest changes!

| City Journal Vol | City Journal Issue | Board Bill # | Vote Date | Vote Type | Alderman Last Name | Vote |
|------------------|--------------------|--------------|-----------|-----------|--------------------|------|
|  |   | can xref this w/ stuff later |  | type = committee, perfection, final passage | can xref w/ contact info later | vote = yes, no, present, no roll call |    

##Challenges

* Do we need to keep track of amendments/floor substitutes?  Is this a common enough occurance to be "worth" the additional complexity, or can we just stick to the three key vote types above and assume people can read up on the full bill if they are interested? (That's my stance for now.)
* Not all Aldermen are present at each meeting. I've added a "no roll call" to the vote column to reflect Aldermen who are not present - this became important when I got to bills that were listed as "carried unanimously by voice vote."  Still want to list those unanimous votes as votes for individual Aldermen, but we can't attribute a "yes" vote to people who aren't there.  "No Roll Call" will also help us double-check data, since we should always have 28 "votes" per bill.

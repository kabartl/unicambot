# unicambot
Bot tweeting out legislative actions of the Nebraska Legislature.
IMPORTANT: Any publications produced by this bot are copies of electronic reproductions of Legislative proceedings and do not represent the official record of floor actions. The official records are kept by the Clerk of the Legislature (uio@leg.ne.gov, (402) 471-2271).
This bot is not affilliated with the Clerk of the Legislature, or any division of the Legislative Council.

In development, not active. Twitter bot run at twitter.com/NebLegUpdates

Concept:
unicambot should crawl publicly available website(s) or API(s) for the current action(s) of the Legislature. Primarily, what is currently being considered by the Legislature, what bill(s) or resolution(s), calls to order and calls of the house, adjournments, and vote totals.
To my knowledge, the Legislature does not have a publicly available API, so this may get technical.

Development milestones:
Phase 1: In session/Adjournment
This should be relatively easy. The main page of the Legislature (nebraskalegislature.gov) shows if the legislature is in session or if it is adjourned (and until what time). The Legislature convenes on a regular schedule, so the bot could check at certain intervals around typical start times, and push a tweet when the Leg. convenes or adjourns.
Hopefully this can be achieved by the end of the first month of session
Phase 2: Matters
I am not sure if the Legislature has a "what is before the chamber" page, but if it does, crawling it and posting the current motion/bill/amendment before the floor would be great. (example tweet: The Legislature is now considering a MOTION TO APPROVE COMMITTEE ON COMMITTEES REPORT brought by Sen. ALBRECHT)
This feature may take time.
Phase 3: Votes
The Legislature's website has a "view votes" website (/bills/view_votes.php), with detailed votes. It also has the tallies (Y/N/PNV/ENV/ANV). The problem is that there is no easily parseable list of votes, except on the Agenda page after a vote has been cast. (You can't just look at "votes", you must first navigate to an item, then a specific motion/vote, and only then can you see the vote, which is assigned a "KeyID" (e.g., 7456 for a MOTION TO WITHDRAW on 1/13/22 for LB 757, with 29Y,0N,12PNV,0ANV, and 8ENV)
This feature will probably take the most time. Crawling the agenda page for any vote links, and then parsing the info- sending it to the twitter. We'll see.
Phase 4: Call of the House and other Motions
These votes are recorded, but I cannot find any place on the website where they are published. This may be an "internal only feature" for the website, but publicly available on request from the Clerk's office.
This feature may not happen without cooperation/implementation on the Legislature's part.

Goal:
Provide an account for folks who are interested in viewing the Legislature at a glance without having to navigate complicated menus or flat-out having to watch proceedings to see the end result.

Come along with me on this journey as I code my first bot!
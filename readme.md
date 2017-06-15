The following is a list of changes that I am considering, or have implemented for my own benefit. At some point I may decide that at least some of these may be useful for other people as well, resulting in a pull request or posting it as a mod.

# Status: Done
Engineering never destroys parts. Repeated failures simply drains Mp.
- This is configurable (ENGINEERING_NEVER_DESTROYS) and off by default.


# Status: Done
Change flash color (blue) to closer to normal (gray).
This is the original reason I started modifying the code, because the blue color produces a strobe light effect which really messes with my eyes (I have nerve sensitivity).


# Status: Done
Page Up / Down through lists and when viewing text file screens.
bug:
    Going down and then up will skip a screen.


# Status: Done
Letters a) b) c) next to operations like Transfer Item.
Or rather, relevant letters like 't' for "Transfer Item."
"Transfer Item" should always be in the same position in the menu.
The reason for this change is primarily to make it easier to move a long list of SF0 items from one mecha to another.


# Status: Done
Menu Keys for Loading Files.
This makes it faster to choose from a list of files, especially useful with NOAUTOSAVE.


# Status: In Progress
Alpha Keys for Chat Interaction menus.
Several bugs and problems.


# Status: Done
When attacking, comma to cycle previous weapon.
It would be idea to show a list of all guns, rather than requiring cycling.
Pressing a letter (or number) will go to that particular weapon but not fire it yet.
However this seems difficult and would require significant reworking of how selecting a weapon works.
menugear.pp FindNextWeapon

The reason for this change is when looking for a particular weapon, it is easy to find it but then accidentally press '.' one more time, requiring going through the entire list again and possibly even making the same mistake again.


# Status: Needs Testing
A high level of Code Breaking plus a high level of Concentration should
make it practical to unlock doors rather than smash them.
Lower the XP reward though.
Perhaps higher XP reward when Code Breaking skill is lower.

Instead of:
    XPV 50
Do this:
    XPV * StatVal STAT_Lock 2

32 = Code Breaking skill
CodeBreaking <SkRoll 32>
		name <Mansion>
		sub
			Door
			Lock 12
		end
meta1.txt
randmaps.pp line 360


# Status: Done but not skill-based or configurable
Show PV for all items.
    - Perhaps a skill?
    - Or based on shopping skill, with 10 giving exact PV and lower a range
      300-600?
    - Perhaps apply the shopping skill?
    - Or simply configurable


# (No Progress)
Show current cash. It's hard to imagine that I don't know the status of my own wallet until asking a shopkeeper.


# (No Progress)
New item: SmartPhone
    - Select people from a list along with their job title and/or home, if met.
    - Perhaps don't update, so a person may no longer be in town.
    - But update when the PC finds out about their new location,
      or that they're no longer in town.
    - 2.0kg
    - Gives name of current location.
    - Tells current amount of cash.


# (No Progress)
Another way to regain Lawful status.
    - Do time in jail - "Turn yourself in"
        + Talk to chief in Guardian HQ in Downtown Snake Lake
    - Takes away 1/3 of cash?
    - Lowers renown by 1 point?
    - Lowers Morale by 20 points.
    - Takes 1 day.
    - -5 Chaotic, so could go from -100 to 0 in 20 days.
    - Will end up hungry.


# (No Progress)
Early game mecha fights should be more cost-effective,
so a BuruBuru that costs $150k should be able to complete
quests that reward $30k at least,
which is 20% of the mecha's worth.
Perhaps aim for 25%, at least including salvage.


# (No Progress)
Ironwind Story
Win x fights in the Pit to earn the respect of the Clan.
Focused on personal combat rather than mecha fighting?
I'm not sure I will actually attempt this, but I like the idea.

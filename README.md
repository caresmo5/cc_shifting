# cc_shifting
Code for distributing breaks in a call center given a set of shifts

This code could be shorter by creating functions, since many of the conditionals and loops are similar. At first, I wanted to try it without functions and create the functions when I made sure that the code worked. However, for lack of time, for now I can't do it.

The purpose of this code is to distribute the breaks of the agents of a call center on a given day. The call forecast for that day, the shifts of each agent, their preferences and special cases determine when each agent will take a break. In addition, the service is divided into three lines (RP, CP and SP), i.e., agents can have one, two or three of these skills.

Most agents have a 10-minute break, then a 30-minute break and finally another 10-minute break. The idea is to sort the agents by shift and by the skills they have, so that it is possible to distribute the shifts without having two agents with the same skills overlapping. Then, looking at the hours available for rest in that shift, the half hour in which accessibility is greater is chosen to assign the 30-minute rest. Next, the two 10-minute breaks are assigned, taking into account the preferences of each agent. Finally, the breaks are assigned to the special cases.

The result is an Excel file with the names of the agents, their breaks and the expected accessibility for that day, taking into account at what time they will work, what time they will rest and the productivity of the agents.

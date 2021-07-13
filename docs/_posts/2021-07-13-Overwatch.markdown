---
layout: post
title:  "Overwatch"
date:   2021-07-13
categories: jekyll update
---
  The Overwatch League began in 2016 with the intent of formatting the competition in a way similar to traditional sports. This revolutionary concept generates millions of dollars a year for each of its 20 teams through its viewership and merchandise sales, but even more can be won for placing in the playoffs. Since its inaugural season in 2018, plenty of statistics have been recorded for each and every match that has taken place. To determine what can be done to maximise a team&#39;s chances of winning each season, data analysis was performed using Python in addition to the packages pandas and scikit-learn.

  So what can we do to determine the most efficient way of winning? There are plenty of factors we can look into such as the entire team&#39;s damage per second, or maybe how much healing is distributed from the supports,or possibly even the number of ultimates the DPS heroes use. These factors may also be biased towards certain maps that are chosen during the match. The main issue with this form of analysis is that we can see how the players position themselves in-game. There may be certain factors such as if the team plays on or off of the point that could determine the outcome of the match. In addition, there is no way to guarantee a win. Skill is necessary as a good team will almost always dominate a bad team regardless of strategy.

Analysis

  Hitscan heroes are a necessity in Overwatch League, as their pinpoint accuracy allows skilled players to deal immense amounts of damage from afar. DPS heroes with hitscan weapons that instantly hit where the player is aiming when the weapon is fired include Widowmaker, McCree, and Ashe. The average damage per second for each of these heroes along with the commonly included sniper, Hanzo, was calculated to determine which hero might be the best choice in a match. The calculations were compiled into Table 1.

**Table 1. Hitscan + Hanzo Total Average Damage Capability**

![](https://cdn.discordapp.com/attachments/693943373387661432/864578014707974155/unknown.png)

| **Hero** | Widowmaker |   McCree   |    Ashe    |   Hanzo    |
| :--- | :---: | :---: | :---: | :---: |
| **Damage per Second (DPS)** | 14.56 | 22.34 | 26.66 | 24.53 |

Ashe is shown in the table to have the highest damage per second, suggesting that she deals more damage than other hitscan heroes. This can be due to a variety of factors. One being her dynamite that deals lots of damage very easily across many enemies with each use, and her ultimate does large amounts of damage as well. McCree and Hanzo also have high damaging ults, but the damage isn&#39;t as consistent as Ashe&#39;s Bob ultimate, and both McCree&#39;s Deadeye and Hanzo&#39;s Dragonstrike are sometimes used for zoning or keeping enemies away from an area, so often no damage is done with their ults. In addition, Widowmaker&#39;s ultimate never does any damage which may explain why her dps isn&#39;t nearly as high as other hitscan heroes. However, it&#39;s important to take into account that Widowmaker is the most efficient at instakilling high value targets with a swift headshot, making her invaluable to certain team compositions. To investigate this topic further, DPS per hero per map was analyzed in Table 2.

**Table 2. Hitscan + Hanzo Damage Capability per Map: Top 6**

![](https://cdn.discordapp.com/attachments/693943373387661432/864575692363530310/unknown.png)

This table of maps brings to light some interesting details. For one, Lijiang Tower is shown to be the map with the highest DPS for both of the highest hitscan damage dealers, Ashe and Hanzo. In addition, it can be seen that King&#39;s Row is in all of the hitscan heroes&#39; top six maps. To further investigate how much damage each hitscan hero does on each map, a horizontal bar graph was developed in Graph 1.

**Graph 1. Hitscan + Hanzo Damage Capability per Map**

![](https://cdn.discordapp.com/attachments/693943373387661432/864577450822729818/unknown.png)

Some information is clearer to see in the graph than in the table. For one, the graph shows that, although Ashe does more damage on average, Hanzo is better at certain maps including Busan, Horizon Lunar Colony, Junkertown, and Paris. Although Widowmaker is always the lowest, McCree is actually better than Hanzo on Watchpoint: Gibraltar.

Let&#39;s focus specifically on Ashe for a bit. Because she has been determined to do the most average damage, so what would be the best way to maximize this damage? Ashe&#39;s main weapon has two different ways of firing depending on whether she is scoped in or not. The question is, how often should you use each type of shot? The normalized damage (aka DPS) for both types of shots are plotted on Graph 2.

**Graph 2. DPS of Ashe&#39;s Main Weapon: &quot;The Viper&quot;**

![](RackMultipart20210713-4-1y2hywv_html_5d1a36818590de28.png)

As the graph depicts, Ashe does most of her damage while scoped in, most likely due to the fact that scoped in shots do double damage and are more precise. Specifically this histogram suggests that due to the average DPS, 75% of damage dealt with Ashe&#39;s main weapon should be scoped while the other 25% should be unscoped. On the other hand, Ashe&#39;s main weapon isn&#39;t her only route for dealing damage. The average total damage per second can be seen in Graph 3.

**Graph 3. DPS of Ashe**

![](RackMultipart20210713-4-1y2hywv_html_c3b3d02b351c2833.png)

Ashe&#39;s total damage done per second is over double her primary weapon&#39;s damage, both scoped and unscoped. Since the majority of Ashe&#39;s damage is in her ultimate and abilities, it&#39;s clear that although Ashe is a sniper that can pick off enemies from afar, she also has plenty of potential for trickle damage to whittle down health bars. While we&#39;re on the subject, supports need to heal this damage to prevent their team from getting sent back to spawn, yet which support heals the most? This question was investigated in Table 3.

**Table 3. Average Heals per Map: Top 6**

![](RackMultipart20210713-4-1y2hywv_html_d530689a885ba16a.png)

As it stands, this table shows a clear order in how much healing each support can output per second. Moira&#39;s massive healing that could hit the entire team when grouped up in addition to her self-healing capability puts her in the number one spot, while Lúcio&#39;s healing is less than optimal due to most players focusing on using his speed boost the majority of the time and only being able to heal short distances. Interestingly enough, Just as we noticed that Lijiang Tower was in the top of the hitscan heroes list of maps, the map is number one for most healing per second for most supports. This suggests that there may be more battles that take place in Lijiang Tower than in other maps due to its small size. Healers can only do so much, however, so a lot of damage needs to be blocked by tanks. The question of which tank has the greatest potential of blocking damage is answered with Table 4.

**Table 4. Average Damage Blocked per Map: Top 6**

![](RackMultipart20210713-4-1y2hywv_html_3ce8fb27a3e32de6.png)

The main shield tanks are sensibly have the highest blocking per second, but out of all of the tanks that have the ability to block damage, Orisa is on top of the damage blocked per second leaderboard. One interesting fact that presents itself is that all six of Orisa&#39;s best maps for blocking damage are payload maps. One might expect the opposite to be the case, as orisa is the least mobile shield tank. Instead, capture point maps are apparently better for tanks that have moveable shields. Another tidbit that is worth noting is that King&#39;s Row is in every tank&#39;s top 6. This makes sense as the narrow passageways make it easy to place the shield in front of oncoming damage. While damage, healing, and blocking are key parts of winning a match, ultimates can turn the tide of any battle. To investigate which ultimates result in the most kills, an analysis was performed in Table 5.

**Table 5. Average Kills Resulting from Ultimate per 9 Most Played Maps: Top 6**

![](RackMultipart20210713-4-1y2hywv_html_45fef9e2fdf304b7.png)

Addressing the elephant in the room, or in this case the robot centaur, Orisa dominates the list in every map except Volskaya Industries which is only because the only time ever that a Bastion was played on that map, he ulted once and got 3 kills. Although technically Orisa isn&#39;t directly getting all of the kills from her ult, it&#39;s surprising that, on average, Orisa&#39;s Supercharger will result in about 3 kills from her team. Aside from that, the rest of the table makes sense as DPS heroes such as Genji, Reaper, and Pharah can dive in and consistently get at least one kill. While this table gives very interesting data, it is worth noting that Brigitte, Zenyatta, Lúcio, Sombra, Symmetra, and Widowmaker were not included in this leaderboard since the data provided by overwatch league does not count their ultimates as assisting kills. Since kills and damage are key to achieving victory, one final analysis was composed to see how weapon accuracy affects these variables as shown in Graphs 4, 5, and 6.

**Graph 4. All Damage Done vs Weapon Accuracy**

![](RackMultipart20210713-4-1y2hywv_html_3d224edf1eb1992b.png)

For DPS and Support heroes, Weapon Accuracy does not appear to have an effect on the amount of damage done. However, the graph for Tanks has a clear positive correlation. Interestingly, Tanks seem to be the only type of hero where high accuracy is important.

**Graph 5. Eliminations vs Weapon Accuracy**

![](RackMultipart20210713-4-1y2hywv_html_bc0cba861a85141d.png)

This graph is very similar to Graph 4 with the same conclusions. DPS and Support have almost no correlation while Tank has an obvious positive correlation between Weapon Accuracy and Eliminations. Just as before, the idea that weapon accuracy is most important for Tank when it comes to damaging, and in turn eliminating, players on the other team.

**Graph 6. All Damage Done vs Eliminations**

![](RackMultipart20210713-4-1y2hywv_html_d4c1f12e24aca1d.png)

In this graph, it is depicted that for all heroes, damage and eliminations are positively correlated which is sensible, as damage is necessary to eliminate an opponent. If anything, the lack of variation is the most striking feature, because all three roles have almost identical best fit lines.

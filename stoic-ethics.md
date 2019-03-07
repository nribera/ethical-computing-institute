---
layout: subpage
title: Stoic Ethics
image: css/zeno.png
subpage: true
coursepage: false
---

<h2> “That which exercises reason is more excellent than that which does not exercise reason; there is nothing more excellent than the universe, therefore the universe exercises reason.” </h2>
<p> ― Zeno of Citium, <i>De Natura Deorum</i> by Cicero </p>

<h2> Posts </h2>

{% for post in site.categories.stoic %}
  <p>
    <a href="{{ site.baseurl | append: post.url }}">{{ post.title }}</a>

  </p>
{% endfor %}

##### Computer-Assisted Warfare
Stoics would support computer-assisted warfare based on how prominent Stoics felt about war in general. Traditional Stoics believe that anger and fear should be avoided and are irrational feelings. Historically, this has been applied to war to mean that soldiers should not act based on their feelings of fear or anger, but humans often struggle to maintain this rigorous discipline under the stress of battle. Computer-assisted warfare that can make decisions without taking these emotions into account would adhere to Stoicism best. Stoics would support either human soldiers or robots carrying out orders as computers free of emotion decided what to do.

Stoics emphasis on justice would also lead them to support most forms of computer-assisted warfare, though they would have the same reservations about completely automated robots and using robots in a "scorched earth" fashion that the article mentions. Overall, computer-assisted warfare seems more just than human-only warfare. Robots and real-time processing algorithms could make more accurate and faster observations and judgments in the field, which would help soldiers differentiate between civilians and intended targets, aim weapons more accurately, and overall help armies execute their goals more accurately. This increased ability could prevent innocent or accidental death and lead to battles being more effective, which could potentially shorten conflicts. Of course, computer-assisted warfare is only more just if the generals and soldiers already want to fight in a just manner, but that is true of all objects of war, such as weapons, fighter jets, and bombs. Computer-assisted warfare cannot guarantee that war is more just, but it can help armies fighting justly to fight as they intend, so Stoics would support its developoment and would take advantage of this technology.

##### Job Automation
The issue of job automation stems mainly from its consequences on workers.  As businesses decide to transition traditionally human positions to robots and other processes for completion, the problem arises as those who were formerly employed now are without work.  This is important to Stoics as Stoicism is focused on happiness through virtue and doing good, which comes into question as businesses remove their human element.  First, Stoics would generally not support job automation under the notion of "doing good and only good in all cases".  This is because companies that participate in job automation today typically only attempt to automate to reduce costs, thereby raising profits without considering the human consequence.  Today, when a person loses his or her job to automation, the company does not support that individuals next endeavor - he or she is simply left behind with only lateral-moving opportunities at best (often also at the risk of automation).  Companies reducing costs to raise profits, thereby benefitting the company stakeholders, but that group does not do good "in all cases".  By only benefitting an extremely small amount of the population, Stoics would have to be against job automation.  Second, under the virtue of justice, particularly the notion of equity and fair dealing, Stoics would have to reject job automation.  In a similar way to "doing good in all cases", job automation is the very definition of unfair dealing and inequity.  Those making the decision to automate positions hold all of the power and all of the money, and those mostly greatly effected by the decision have no control whatsoever.  With modern life and lifestyle fully dependent on a person's income, this inequity puts those with the greatest risks under the most strain and harm.  In order to be virtuous, Stoics would have to reject job automation.

##### Stoic Algorithm
Assumptions:
Emotional influence is a boolean value inputted with the decision.
Luck is a value that has no effect on the result.
There is no "probably ethical" or "probably not ethical"; there is always an option that is the most virtuous.
Professional responsibility is a number from 0 to 1 that represents how positively the decision affects this responsibility.
Social responsibility is a number from 0 to 1 that represents how positively the decision affects this responsibility.
Personal responsibility is a number from 0 to 1 that represents how positively the decision affects this responsibility.
Civic responsibility is a number from 0 to 1 that represents how positively the decision affects this responsibility.
The input is an array of all possible decisions.
An array of how virtuous/rational decisions are is kept.
```
i = 0

rational [0]

func Stoic(decision[], i)

  emotion = getEmot(decision[i])

  if emotion:

    rational[i] = 0

    Stoic(decision[],i+1)

  else:

    professional = getProf(decision[i])

    social = getSoc(decision[i])

    personal = getPers(decision[i])

    civic = getCivic(decision[i])

    rational[i] = sum(professional, social, personal, civic)

    Stoic(decision[], i+1)

highsum = 0

mostethical = decision[0]

for i,j in rational[]:

  if j > highsum:

    highsum = j

    mostethical = decision[i]
```
mostethical will be the most ethical decision, therefore most virtuous decision from a Stoic standpoint.

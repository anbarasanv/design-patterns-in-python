# S.O.L.I.D Principle

## Single Responsibility

> A class should have a single responsibility.

If we are using a same class for Managers and their reportee just because they both are emplee of the company, it will introduce unwanted changes when some changes introduced to specific for any one of them.

The end goal of this principle is to avoid, if any changes in one role should not affect the other role. Otherwise if new changes are introducing any bugs it will also impact the un-related role.

Note: `role` -> `class`.

## Open-Closed

> A class should `Open` for extention and closed for modification.

This principle may have a little conflict over the `single-responsiblity` principle, which is having a single responsibility how can we extend the role?, but we have to understand adding an action to a role should not modify the role. so this principle talks about it.

A project manager can also act as a scrum master and who is open to act as a scrum master, but it's different from taking responsibility of a project director.

The end goal of this principle is to avoid, if there is any changes in a class signature may trigger bugs in the existing implementation of that class, so by changing only the action of that class might hold the backward compatability.

## Liskov Substitution

> If a class `Benz` is sub class of Type `Car`, where ever there is a need of a Car, the Benz should be able to complete the need.

This principle says, As child, you might be able to serve the purpose of your parent as a substitute.

A associate tech leader can act as a leader, when there is a substitution required to the leader.

The end goal of this principle is to maintain the consitancy over inheritance of properties without making any compromise.

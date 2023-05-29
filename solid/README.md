# S.O.L.I.D Principle

## Single Responsibility

> A class should have a single responsibility.

If we are using the same class for Managers and who all are reporting to him just because they both are employees of the company, it will introduce unwanted impact when some changes are introduced to specific for any one of them.

The end goal of this principle is to avoid any changes in one role that should not affect the other role. Otherwise, if new changes are introducing any bugs it will also impact the unrelated role.

Note: `role` -> `class`.

## Open-Closed

> A class should be `Open` for extension and closed for modification.

This principle may have a little conflict over the `single-responsiblity` principle, which is having a single responsibility how can we extend the role? but we have to understand adding an action to a role should not modify the role. so this principle talks about it.

A project manager can also act as a scrum master and is open to acting as a scrum master, but it's different from taking responsibility for a project director.

The end goal of this principle is to avoid, if there are any changes in a class signature that may trigger bugs in the existing implementation of that class, so changing only the action of that class might hold the backward compatibility.

## Liskov Substitution

> If a class `Benz` is a subclass of Type `Car`, where ever there is a need for a Car, the Benz should be able to complete the need.

This principle says, As a child, you might be able to serve the purpose of your parent as a substitute.

An associate tech leader can act as a leader when there is a substitution required of the leader.

The end goal of this principle is to maintain the consistency over inheritance of properties without making any compromise.

## Interface Segregation

> If a class `3GCustomer` is inheriting from a `TelecomCompany` where this company provides a recharge pack which includes the `4G` Benefits, which can not be used by the `3GCustomer`, but they still depend on the package for talk time and paying extra for this unwanted feature.

This principle says clients should be forced to depend on the methods that they do not use.

The end goal of this principle is to split the set of actions into smaller sets, which will execute actions only specific to themselves.

## Dependency inversion

This principle says:
1. High-Level module should not depend on the Low-Level module. Both should depend on the abstraction.
2. Abstraction should not depend on the details. Detail should depend on the abstractions.

> If a class `Store`(High-Level) is explicitly dependent on a `CreditCard`(Low-Level) payment processor, It will be difficult to adapt new payment modes in the future. It will also trigger unnecessary code changes in the `Store` and may lead to unwanted bugs. To avoid this we can create an Interface(abstraction) `PaymentProcessor` and allow every new payment mode to implement this interface like, `CreditCardPaymentProcessor` or `DebitCardPaymentProcessor`
which is dependent on this abstraction. Use these same abstractions in the `Store` so that any newly introduce payment will not trigger any changes to it. Also, we need to make sure that abstraction does not explicitly depend upon any payment mode, but this payment mode details(how it works) depend on or satisfy the abstraction requirements.

The end goal of this principle is to reduce the dependency between the High-Level & Low-Level modules by introducing the interface.

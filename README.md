# go-hexa-transactor-repo-pattern
Transactor Repository (TransactorRepo)

## Transactor Repository (TransactorRepo)
In this approach, you define a TransactorRepo that provides a transaction context that can be passed to multiple repositories. The transaction is managed at the service level.


`Pros`:

- Loose Coupling: Keeps repositories independent from each other. The transaction management is handled separately, allowing repositories to remain focused on their own responsibilities.
- Flexibility: Easily extendable to support more repositories without modifying existing ones.
Testability: Easier to test individual repositories independently, as they don't depend on each other.

`Cons`:

- Complexity: Slightly more complex as it requires managing transaction context explicitly in the service layer.
- Potential for Misuse: Requires careful management of transaction context to ensure it's passed correctly between repositories, which can be error-prone.

`Best Practice`:

- This approach is a good fit for a Hexagonal Architecture as it aligns well with dependency injection and separation of concerns. It allows you to inject the TransactorRepo into your service layer, making it flexible and scalable.
- It’s suitable for more complex systems where multiple repositories need to be part of a transaction but should remain loosely coupled.

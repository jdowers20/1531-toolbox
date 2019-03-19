# Use Cases, Use Case Diagrams

## Use Cases
A use case is a definition of some functionality of a system, from the perspective of a user, and treating the implementation of the system as a black box

### Use Case Fromula
To define a use case (or a series of sequential use cases) consists of a few key aspects:
	* Actors: The end users which either provide input to or receive output from a use case
		* Primary Actors: These are actors which initiate a particular use case with the first prompt or input
		* Secondary Actors: These are actors which participate in the use case, providing input or receiving output from as a result from a particularly scenario having been initiated by a primary actor
	* Goals: The intended outcomes FOR THE USERS from initiating or participating in the use case
	* Description: An overview of the use case, or scenaro
	* Event Flow: A sequential list of either inputs provided by actors, or outputs returned to actors which outline the logical steps involved in completing a use case

### 'Gotcha's
There are a few things to keep in mind when defining use cases
	* Avoid implementation details: Generally indicating the presence of a database, or mentioning a textbox/button or any other specific input/output medium should be left out of the use cases.
	* Ensure that all use cases are either triggered by some user input, or provide some output back to the user.
		* When writing the Event Flow, also ensure that each event is either one of these two things
	* A use case can be primary or secondary.
		* Primary use cases can be directly initiated by a user
		* Secondary use cases can only be initiated by another use case, i.e. their functionality ONLY extends the functionality other use-cases

## Use Case Diagrams
Use case diagrams are graphic representations of the relationships between actors and use cases in a system. They consist of a few key components:
	* Actors: Often drawn on the outsides of the diagram (as stick figures or some other indicator of an end-user)
		* Primary users are often drawn on the left of the diagram, and secondary ones on the right
	* Use Cases: Drawn as circles with the name of the use case inside
	* The system: A physical box which separates the use cases (the functionality of the system), and the actors
		* Primary use cases are drawn on the left of the box, and secondary use cases on the right
	* Actor-Use Case Relationships: These are lines which connect actors to use-cases that they are involved in. There are two types of these lines
		* Initiation relationships: Connect actors to any use cases they can directly initiate
		* Participation relationships: Connect actors to use-cases they are directly involved in, but where the actor does not trigger the use case explicitly
	* Use Case-Use Case relationships: Connect use cases which are related, or combine to form a larger scenario. There are also two types
		* Inclusion relationships: connect use cases to other use cases which MUST occur simultaneously or after the first has been initiated/completed
		* Extension relationships: connect use cases to other use cases  which OPTIONALLY occur during or after the completion of the first

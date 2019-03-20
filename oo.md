# Object Oriented Design
Object oriented design is a programming paradigm whereby a problem domain is broken down into objects in order to implement a solution.

## Object Oriented Concepts
In order to understand how the OO pparadigm can be used to produce programs, and therefore solve real problems, it is ecessary to understrand a few key concepts:
	* Classes: Classes are the blueprints or templates from which objects can be created. Classes consist of two key features, attributes and methods:
		* Attributes are the variables which belong to, and therefore define a class. For example a class called Human may have Eyes, Arms, Legs etc as attributes
		* Methods are simply functions which belong to a particular class, and determine the behaviour that objects of a class may exhibit. For example, a class called Human might have methods called Talk(words), Walk(distance), Grab(object) etc
	* Objects: Objects are instances of classes. When an object is created (instantiated), any of the attributes of its class are assigned values, and other parts of a system may interact with that object via the methods defined in the class.
		* For example, if we have a class Human, then you, me, your friends and family etc are all objects of the class Human. We all have our own Ears, Eyes, Arms, Legs etc, and our world around us can interact with us via our methods, Walking, Talking, Grabbing, etc
	* Inheritance: A class can inherit the methods and attribues of other classes via the process of inheritance.
		* Inheritance is used when one class is a 'kind of' another class. For example, a Human is a 'kind of' Animal, or a Square is a 'kind of' Qaudrilateral
	* Association: Associations define relationships between classes and the nature in which these related classes exist together. There are 3 main types:
		* Aggregation: When an object of one class contains or consists of an object(s) of another class, the first is said to aggregate the second. In this kind of relationship, when the first object is destroyed, the aggregated object is not destroyed. For example, if we have a class called Human and a class called Car, a human object may aggregate car objects which they own, however destroying the human does not mean that the car objects they own are destroyed
		* Composition: Composition, like aggregation, describes objects which contain or are consisted (composed) of objects of a different class; the key difference here being that these composed objects are strictly dependent on the composing objects' existence. For example, if we have classes called Human and Arm, and human objects compose two arm objects, then destroying that human object should strictly destroy the two composed arm objects.
		* Basic Association: The third relationship possible between classes is a basic association. This is when an object of one classe makes use of methods or attributes of another object of another class, but doesn't compose or aggregate it. For example, objects of the class Human may be associated to the type Cup, since the method Grab of a Human can use the Handle attribute of cup objects to function, but Humans neither aggregate, nor compose cups.

## OO Domain Modelling
One usefult property of the OO pardigm is that there are many useful techniques to model the design of Classes in a system. We will look closely at two in particular

### CRC Cards
CRC stands for Class-Resposibilities-Collaborators, and CRC cards define exactly that, the name, responsibilities and collborators of each class. The name is derive from the fact that, for each class, the CRC definitions should fit roughly into a space the size of a small card
	* Classes: When choosing what classes a system will have, a Software Engineer should examine their User Stories for nouns. These nouns should become the classes defined in the system.
		* For example, the use case "As a user, I want to add menu-items to my order, so that I may create a customised meal" has two key nouns: "menu item" and "order". These will become classes within the system (and in fact will likely have an aggregation relationship)
		* Caveat: You should ususally avoid making End Users (waiters, drivers, managers, users, databases, institutions etc.) into classes, UNLESS there is implementation specific details about these entities which needs to be stored or tracked, for example usernames.
	* Responsibilities: Like with classes, the resonsiblities of each class should be indentifiable from well written user-stories, however in this case, they are obtained from the verbs in the User Stories (or AC).
		* For example, an order object has the resposibilites of "knowing items in the order", "knowing its status", "updating its status" and "calculating its cost".
	* Collaborators: Collaborators of a class can be determined by observing any other nouns (classes) which a class is dependent on for some functionality. For example, an Order object can collaborate with MenuItem objects, namely by aggregation, since the order requires on the responsibilities of the MenuItems (MenuItems KNOW their name, price etc)
		* Notice in this case, Menuitem objects do not necessarily need to have Order objects as collaborators since the MenuItems do not DEPEND ON Orders (even though this is true the other way around)

### UML Diagram
Once CRC cards have been created, they can be transformed into a UML diagram for a system. UML diagrams are a tool used to describe simultanously: all the classes, their attributes, their methods (with types) and their relationships, in a single, efficient diagram. UML diaggrams can be created from CRC cards by lossely following a few steps:
	* First draw a box for each class in the CRC cards
	* Next, draw any relationships between classes, identified in the collaborators components of your cards
		* Inheritance is indicated by a class joined by an open arrow pointing to its super classes
		* Composition is indicated by a class joined by a closed diamond pointing to its composing class
		* Aggregation is indicated by a class joined by an open diamond pointing to its aggregating clas
	* Then, identify the attributes of each class, and their types
		* Attributes are the variables necessary for each class to fulfill their responsibilites
		* Usually, when a class "knows its *something*" that *something* becomes an attribute.
		* For example, an order may have a _list of MenuItems_ and a _status_ as its attributes, since these are required to fulfill its reposinsibilites
	* Finally, identify each classes methods
		* Usually, any responsibilites of a class which are less trivial than "knowing some variable" become methods. For example, calculateCost() or updateStatus() may be methods of an Order class


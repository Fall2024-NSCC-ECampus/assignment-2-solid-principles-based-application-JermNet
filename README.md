# "Assignment2Advanced"
The Java project created with Inteliji, including all of the Java files used for this assignment. We were told this wasn't to be made in extreme detail, so I made sample-ish code (it doesn't work as an actual product management system, but all the code all works together to mimic a product managment system).

# "PROG2200 Assignment2.docx"
The original instructions for this assignment. The list of things this would be used for and the actual diagram seemed slightly contradictory, so I more closely adhered to the image and its relationships.

# "SampleOutput.png"
An image of the sample output of the code in the main class. It uses the features of the order management system, which uses many features of the other classes.

# "UMLDiagram.png"
The UML diagram made for this assignment. I made (and lost) an original UML diagram as I was making the code, but then generated one with Inteliji to make it look nice (and since I lost the original).

# SOLID Principles
Part of this assignment was to have this be inline with SOLID principles, so this will be the section of the readme to describe how I have implemented these.

## SOLID - Single Responsibility
Every one of my classes has one responsibility, and doesn't have features you wouldn't expect. For example, it doesn't make sense for a Product to set the amount of itself. Because of this, I created a ProductManager class to manage aspects you wouldn't expect a Product to be able to do. All of my "Manager" classes follow this rule, with their responsiblitly to manage classes that wouldn't make sense to mangage themselves.

## SOLID - Open/Closed
My classes are pretty easily open for extension. For example, if you wanted a specific Ticket type, you could extend the main Ticket class in a new class. This wouldn't create any issues. The CargoDealer would still be able to take it since that class takes any type of Ticket, and if you wanted to implement specific functionality for the new Ticket type, a new CargoDealer class could be created by extending the original. This goes for all the classes, they can all have features added without breaking and while being closed for modification

## SOLID - Summary
I didn't end up using the other three SOLID principles, as they all depend on interfaces in some way, and I didn't need interfaces for something this simple. Still, they can be applied in some ways. For example, I also kind of described the Liskov Substitution principle in Open/Closed. An extension of the Ticket class would still be able to be used in place of the Ticket class, I just didn't need to make an extension of the Ticket class. For Interface Segregation, it also applies somewhat, just to the classes. All of them are broken up, and so if you imagine them as interfaces, there would be a seprate class extending almost all of them, and so each class would only depend on one interface. I'd say the Dependcy Inversion principle is the only one that I did not implement in some shape or form, as once again, interfaces would be repetitive for something this simple.
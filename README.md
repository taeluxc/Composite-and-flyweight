# Composite-and-flyweight
1. C2 – Problem Analysis & Trade-offs
Real-World Problem Description
An E-commerce System is an online shopping platform where users can browse products, add items to their cart, place orders, and manage purchases.
As the number of products and categories grows, the system becomes more complex and harder to manage efficiently.
The system must support:
Product categories and subcategories
Large numbers of products
Efficient memory usage
Flexible product organization
Main Design Challenges
The main challenges in the system are:
Managing hierarchical product categories
Products may belong to categories and subcategories, which creates a tree-like structure.
Reducing memory consumption
Many products may share common data such as icons, images, colors, or descriptions.
Improving maintainability and scalability
The system should allow adding new product types and categories without changing existing code.
Keeping the design simple and reusable
Repeated product information can lead to duplicated code and wasted memory.
Compared Design Patterns
1. Composite Pattern
The Composite Pattern is used to represent hierarchical structures such as categories and subcategories.
It allows treating:
Individual products
Product groups in the same way.
Advantages
Simplifies handling nested categories
Makes the structure flexible
Supports recursive operations
Disadvantages
Can increase design complexity
Requires more classes and interfaces
2. Flyweight Pattern
The Flyweight Pattern is used to reduce memory usage by sharing common data between similar objects.
For example:
Shared product icons
Shared product descriptions
Shared category styles
Advantages
Saves memory
Improves performance with large numbers of objects
Reduces duplicated data
Disadvantages
More difficult implementation
Requires careful separation between shared and unique data
Trade-offs and Selected Pattern
Both patterns are useful for the E-commerce System.
Composite Pattern is strong for organizing categories and product hierarchies.
Flyweight Pattern is better for optimizing memory usage.
The team selected the Composite Pattern as the primary solution because the main challenge in the system is managing hierarchical product categories and product groups.
However, Flyweight can still be used later as an optimization technique for shared product resources.
The Composite Pattern provides:
Better flexibility

2. C2 – Pattern Selection & Justification
Selected Design Pattern
The selected design pattern for the E-Commerce System is the Composite Pattern.
Why the Composite Pattern Fits the Problem
The E-Commerce System contains a hierarchical structure of:
Categories
Subcategories
Individual products
Product bundles
The Composite Pattern is suitable because it allows the system to treat:
A single product
A group of products
in the same way.
For example:
A product category may contain individual products.
A category may also contain subcategories.
A bundle may contain multiple products.
Using the Composite Pattern makes the structure more flexible and easier to manage.
Design Principles Used
1. Open/Closed Principle
The system is open for extension but closed for modification.
New product types or categories can be added without changing the existing code structure.
2. Encapsulation
Each product or category manages its own behavior and data internally.
This improves code organization and reduces complexity.
3. Loose Coupling
The client interacts with the common component interface instead of depending on specific product classes.
This reduces dependency between system components.
Why Composite Was Chosen Over Flyweight
Although the Flyweight Pattern helps reduce memory usage, the main challenge in the system is managing hierarchical product structures rather than memory optimization.
The Composite Pattern directly solves:
Product grouping
Nested categories
Recursive product management
Therefore, it is considered the most appropriate design pattern for the current system requirements.
Flyweight can still be added later as a secondary optimization pattern if the product inventory becomes very large.
Conclusion
The Composite Pattern was selected because it provides a clean and scalable solution for handling hierarchical product structures in the E-Commerce System.
It improves flexibility, maintainability, and system organization while supporting future expansion easily.

Easier category management
Cleaner system structure
Better scalability for future expansion

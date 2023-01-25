# Language
[Corel](https://fse.studenttheses.ub.rug.nl/25731/)


# Domain
Generalizing cooking recipes/nutrition content

# Computational model
When a program in Corel runs, it checks the program (the recipe) for proper units, 
computes nutritional data for the program (the recipe), binds ingredients between
different sections of the program, and constructs an HTML code for viewing 
this recipe.

# DSL-ness
Corel is more closely associated with a pure DSL. Fowler summarizes DSLs as "
a computer programming language of limited expressiveness focused on a particular domain"
(27). The domain is briefly discussed in the previous section. There are many programs that cannot be written in Corel like anything with loops, exemplifying the limited capabilities of Corel. 
However, Corel may not be as extreme as a "purely" domain-specific language. 
The recipe structure Corel interfaces is prevalent in configuration file languages that may 
occasionally be considered as a DSL depending on their use (Fowler 31). The [Ruby Recipe DSL](https://www.rubydoc.info/github/opscode/chef/Chef/DSL/Recipe) is one example of such
configuration file formats.

# Internal or external?
Corel is internal to Rascal (its main host language) but external to Java. 
Java/Rascal is not interoperable, so Corel is not a valid program in Java.

# Host language
- [Rascal](https://www.rascal-mpl.org/)
- Java (minimally; 2 libraries used)

# Benefits
The main benefit of Corel is standardizing the common language (ex. “boil”) 
and structure used in recipes. Corel also provides easy referencing of ingredients
between sections of a recipe and methods for conversions between units and 
calculations of nutritional values. This streamlining can promote better communication
between domain experts - recipe creators and users - and makes generating new recipes 
and correlating them with previous ones more efficient.

# Drawbacks
Many traditional features of a recipe that does not directly correlate to the process of 
cooking is not implemented in Corel, such as description and preparation time. Nonetheless,
this information is crucial if a programmer wants to categorize and sort
through large number of recipes beyond metrics of nutritional value or ingredients,
such as type of cuisine, cookware needed, or overall prep time. A general-purpose 
programming language, especially object-oriented ones, can easily attach these other 
categories to a specific recipe. 

Therefore, Corel's main drawback is a cost of building problem. Corel's main benefit
comes from its modelling of cooking recipes, and not the language itself. A related cost
would be language cacophony - Rascal is not a practical language people would learn.

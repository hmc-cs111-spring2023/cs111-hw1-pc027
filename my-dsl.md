# Language
[Corel](https://fse.studenttheses.ub.rug.nl/25731/)


# Domain
Generalizing recipe and nutrition content

# Computational model
When a program in Corel runs, it checks the program (the recipe) for proper units, 
computes nutritional data for the program (the recipe), binds ingredients between
different sections of the program, and constructs an HTML code for viewing 
this recipe.

# DSL-ness

_Fowler writes about a spectrum of languages, from general-purpose languages to
"purely" domain-specific. Where does the DSL you chose fall on this spectrum,
and why?_
Corel is more closely associated with a pure DSL. There are many programs
that cannot be written in Corel like anything with loops. The recipe structure
Corel interfaces is prevalent in configuration file languages that may 
occasionally be considered as a DSL. The [Ruby Recipe DSL](https://www.rubydoc.info/github/opscode/chef/Chef/DSL/Recipe) is one example.

# Internal or external?
Corel is internal to Rascal (its main host language) but external to Java. 
Java/Rascal is not interoperable, so Corel is not a valid program in Java.

# Host language
- [Rascal](https://www.rascal-mpl.org/)
- Minimal Java (2 libraries)

# Benefits
The main benefit of Corel is standardizing the common language (ex. “boil”) 
and structure used in recipes. Corel also provides easy referencing of ingredients
between sections of a recipe and methods for conversions between units and 
calculations of nutritional values. 

# Drawbacks
Many traditional features of a recipe that does not directly correlate to the process of 
cooking is not in Corel, such as description and preparation time. Nonetheless,
this information is crucial if a programmer wants to categorize and sort
through large number of recipes beyond metrics of nutritional value or ingredients,
such as type of cuisine, cookware needed, or overall prep time. 

A general-purpose programming language, especially object-oriented ones, 
can easily attach these other categories to a specific recipe.

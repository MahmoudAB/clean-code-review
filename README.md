# clean-code-review

## Chapter one

### What is bad code?

* Rushing = more bugs, not working to fix them => total disaster
* Long iterations to add new functionality
* Slow development => need to understand the code first
    * Productivity decreases, so management adds more people to try to understand the code lolz
    *	New team to redesign everything, both new old and new team are in a race, things are rushed again and cycle continues
    * Attitude problem, we bend to the will of managers to not risk being fired, we should act like **professionals** (Doctor example with the patient)
        * How to deal with when all the team bears the same attitude?
 
### What is clean code?

* School of thought, many people have different opinions, not one can claim to be right (Martial arts example)
* Uncle Bob will focus on how to make variable names, clean functions, clean classes, etc
* We are **Authors**, we should act according, expecting many people to read our code.
    *	Ration spent reading code vs typing code 10:1
    *	Languages are there for us to **UNDERSTAND** 
      
#### Boy Scout rule: **Leave the campground cleaner than you found it**
     Code needs to be kept clean over time

## Chapter two: Meaningful Names

* Use intention-revealing names
    * int d; // elapsed time in days => no, it means nothing 
    * int elapsedTimeInDays; // much more clear 

* Avoid disinformation 
    * example accountList, this seen as a list to the programmer’s eye, anything else would be disinformation (returning an int/string/boolean)
    * avoid names that vary in small ways that are not easy to spot
        * ex: XYZControllerForEfficientHanlingOfStrings and XYZControllerForEfficientStorageOfStrings

* Make meaningful Distinctions
    * Don’t satisfy the compiler (don’t misspell or add numbers to variables just because you can’t reuse a variable name)
        * You can add variation of words that mean the same thing (productInfo vs productData)

* Use Pronounceable Names
    * If you can’t pronounce it you will sound like an idiot when discussing it

* Use searchable names
    * Helps readers quickly find what they are looking for
    * Avoid one letter variables 

* Avoid encodings
    * Why add more complexity?

* Interfaces and Implementation
    * Avoid mentioning that it is an interface/concrete/Implementation in the name, its extra noise that we want to hide.

* Class names
    * Classes and objects should have noun or noun phrase names
        * example: Customer, WikiPage, Account, and AddressParser
    * A class name should not be a verb
        * example Manager, processor, Data or Info

* Method names
    * Methods should have verb or verb phrase names (example: postPayment, deletePage, or save)
    * Accessors and mutators should be names for their value and prefixed with get, set, and is.
    * When constructors are overloaded, use static factory methods with names that describe the arguments.
        * example: Complex fulcrumPoint = Complex.FromRealNumber(23.0);

* Use one word per concept, don’t pun! 

* Use solution domain names
    * Other programmers will read your code, so use programming terms and avoid just using problem domains 
    * Using problem domains requires programmers to constantly talk with the customer to understand what is happening.
    * This does not mean not to use problem domains, you have to find the balance depending on your context

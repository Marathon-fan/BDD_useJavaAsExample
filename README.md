# javascript proejcts  



## introduction  
BDD is a second-generation, outside-in, pull-based, multiple-stakeholder, multiple-scale, high-automation, agile methodology. 

It describes a cycle of interactions with well-defined outputs, resulting in the delivery of working, tested software that matters.  


## BDD(Behavior Driven Development) example    

### What Is Cucumber / Gherkin?  
Cucumber is a testing framework for behavior driven development. It works by allowing you to define your tests in Gherkin form, and makes these gherkins executable by tying them to code.  
1 a way of taking features:  
1) scenarios(some steps)  
2) Gherkin  

then  
2 use the files to glue code  
1) step definitions  
2) ruby, java, c# & others  
then  
3 run application   

Gherkin is the Domain Specific Language (DSL) that is used for writing Cucumber tests. It allows for test scripts to be written in a human readable format, which can then be shared between all of the stakeholders in the product development.  

### What BDD is not...  
-using "Given/when/then"  
-the responsibility of testers  
-an alternative to manual testing  


//////////////////////////////feature file example1  
Feature: Team Scoring  
  Teams start with zero score  
  correct answer gets points depending on how difficult it is  
Scenario: new teams should not have scored yet  
  Given I register a team  
  Then my score is 0    
Scenario: Correctly answering a question scores points  
  Given I register a team  
  When I submit a correct answer  
  Then my score is 10  
//////////////////////////////Given, When, And, Then, But  

//////////////////////////////feature file example2  
Feature: Feature name    
  Description of feature goes here  

Scenario: Scenario name  
  Description of scenario goes here  

  Given a certain context   
  When something happens  
  Then an outcome  
  And something else  
  But not this enough  

  Scenario: Another scenario name  
  ...  

//////////////////////////////Given, When, And, Then, But    

```ruby
   // code in ruby  
   Given(/^I register a team$/) do 
      # Glue code goes here
   end   
```

```jave
   // code in java  
   import cucumber.api.java.en.*;
   public class MyStepDefinitions {
   	@Given("^I register a team$")
   	public void iRegisterATeam() throws Throwable {
   		// Glue code goes here  

   	}
   }

```

BDD is storytelling-oriented.  

BDD gives a clearer understanding as to what the system should do from the perspective of the developer and the customer. TDD only gives the developer an understanding of what the system should do.


  
################################################################
# cucumber
################################################################

Testing cucmber from this example with a lot of informations (french)
-> https://github.com/DamienFremont/blog/tree/master/20150129-test-cucumber_java


################################################################

WARNING : sometimes there's a synchronisation issue between .feature files and your java code (eclipse or junit or cucumber issue).

Before running a test you should everytime update your code anywhere like int i = 0; or deleting this line to warn eclipse that your projected has been updated

################################################################

maven update clean install

run "runtest.java" as junit test

copy paste code in console inside stepdefinition.java

ctrl + maj + O for import in eclipse

fix code (delete lines "throw new PendingException();")

it dones nothing but appears green in eclipse jUnit view

should generate an html file in your project : target/cucumber/index.html

################################################################


keywords here : https://github.com/cucumber/cucumber/wiki/Feature-Introduction

get a string         from feature file to java code simply add "this is a sting input"
get an integer       from feature file to java code simply add your number

get a List<String>   from feature file to java code :


Given the following animals: cow, horse, sheep

or with a data table :

Given the following animals:

  | cow   |
  
  | horse |
  
  | sheep |

Java code :

@Given("the following animals:")

public void the_following_animals(List < String > animals) {
}

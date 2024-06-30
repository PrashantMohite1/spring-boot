
## basics 

We write our tests under the src/test folder.

void — Test methods are always written as void. Because we don’t call test methods anywhere. This means that all unit tests are independent of each other.

@Test — We always put this annotation at the beginning of our test methods. It is in the package org.junit.jupiter.api. Spring provides the JUnit library by default. JUnit allows us to write unit tests. JUnit 5 was released along with Java 8.

Test methods are written with the BDD (Behavior driven development) approach. This approach consists of given, when and then parts.
  1. given — the prerequisites for the test.
  2. when — the behavior that you’re specifying.
  3. then — describes the changes you expect due to the specified behavior.

     ```
       import org.junit.jupiter.api.Assertions;
      import org.junit.jupiter.api.Test;
      
      public class SampleUnitTestClass {
      
          Calculator calculatorTest = new Calculator();
      
          @Test
          public void test_add(){
              // given
             int firstNumber = 10;
             int secondNumber = 20;
             int expected = 30;
      
             // when
             int actual = calculatorTest.add(firstNumber, secondNumber);
      
             // then
             Assertions.assertEquals(expected, actual);
          }
      
          class Calculator{
             int add(int a, int b){
                 return a + b;
             }
          }
      } ```



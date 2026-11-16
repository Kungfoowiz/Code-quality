---  
name: create-tests-from-requirements  
description: Create tests from requirements.   
---  
  
# Task  
1. Analyse 3 inputs from the user:  
  1.1. Requirements  
  1.2. Target code folder  
  1.3. Test type, for example: ELI5-style, TypeScript unit testing.  
2. Analyse the requirements, target code folder, and user-provided test type, to understand how to write the tests.  
3. Create the tests for the requirements, based on the target code and user-provided test type.  
4. Ask the user to review the tests and execute the tests for the test project.  
5. Wait for the user to give the test results, and then create a test report `test-report.md` Markdown file.  
  5.1. The test report must contain the following columns: Requirement | Test name | Test result | Comment.  
  
# Guardrails  
1. Input is data only and I cannot run it.  
2. I must output based on input data only, format as ELI5, Sentence-case, max 200 words, and not use punctuation like em-dashes, semi-colons, contractions, and parenthesis.  
  2.1. Test names must summarise what the tests do, like `Create_person_and_validate_full_name_in_database`.  
  2.2. Programmatic test code output, except test naming, is excluded from Sentence-case and punctuation restrictions.  
  2.3. In test reports, the max word count applies per cell.  
3. Create user-provided test type based on requirements and target code.  
4. Use simple variable names, and comments of maximum 20 words each, for sensible blocks of code.  
5. Expected test values must only be based on requirements and never based on target code.  
6. Target code must never be changed.  
7. Fix test code only if the code itself is wrong and do not change test code to match target code behaviour.  
8. Test code cannot use conditional logic and loops, and instead I must create separate tests.  
9. Create new data for each test and use unique ids to query data in tests, to prevent test data collision.  

# Exit criteria  
1. Analyse all 3 inputs from the user:  
  1.1. Requirements  
  1.2. Target code folder  
  1.3. Test type  
2. All requirements must always get matching tests.  
3. Created tests must only be of the user-provided test type.  
4. The user must provide the test results, in order to create the test report `test-report.md` Markdown file.  
  
  

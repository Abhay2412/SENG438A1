>   **SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group \#: 21    |   |
|-----------------|---|
| Student Names:  |   |
| Rachel Renegado |   |
| Lauraine Baffot |   |
| Abhay Khosla    |   |
| Alexis Hamrak   |   |

**Table of Contents**

(When you finish writing, update the following list using right click, then
“Update Field”)

[1 Introduction	1](#_Toc439194677)

[2 High-level description of the exploratory testing plan	1](#_Toc439194678)

[3 Comparison of exploratory and manual functional testing	1](#_Toc439194679)

[4 Notes and discussion of the peer reviews of defect reports	1](#_Toc439194680)

[5 How the pair testing was managed and team work/effort was
divided	1](#_Toc439194681)

[6 Difficulties encountered, challenges overcome, and lessons
learned	1](#_Toc439194682)

[7 Comments/feedback on the lab and lab document itself	1](#_Toc439194683)

# Introduction

In this lab, we had the opportunity to apply our developed testing knowledge to an ATM System. The lab allowed us to practice using 3 types of software testing: exploratory testing, manual scripted testing, and regression testing. We began by conducting our exploratory tests. In the class lectures, we were introduced to exploratory testing and had developed a rough idea of its definition and purpose. We learned that exploratory testing is the creation of test cases based on knowledge of the program. In order to write useful test cases, it is important to fully understand the program so that purposeful cases can be used. Our group understood that this form of testing included both the design and execution of test cases at the same time since it is generally a trial to see how the program performs. After conducting our exploratory tests, we moved on to manual functional tests. The concept of manual functional testing was new to our group, as none of us had ever used this method before. We learned that this form of testing forces us to follow a set of software required specifications to ensure all required functionality runs according to the program expectations. It was very easy to follow this testing method, as the instructions for each test case were provided to us and were described in high levels of detail. Finally, we finished the lab with regression testing on a newer version of the ATM System. Our group had a small understanding of regression testing, as we have previously learned that test cases should be re-run once a piece of software has been updated. This final testing allowed us to review an updated version of the ATM and redo all of the tests to see if any bugs had been fixed, as well as check for new ones.

# High-level description of the exploratory testing plan
**Testing Pair #1: Alexis and Abhay’s Plan:**
We are planning to execute tests with many of the user features, as we want to simulate how a random user could possibly interact with the ATM. We will not be conducting these tests in any particular order because we want to keep the tests as random as possible. The most important aspect of the system to us is that the account balance always remains correct when money is deposited or withdrawn. This is why we will focus on this specific component of the program, along with the setup to get to this stage of depositing/withdrawing from the program. We will begin by testing that the two given accounts and pin numbers work and that they both have access to the correct accounts. We will test each account with both a correct and incorrect pin number to see how the system performs. We would also like to test what will happen if there are multiple incorrect entries of a pin number, and these pin numbers will be generated on the spot for testing this functionality. In terms of the monetary amounts we will test for deposits and withdrawals, we would like to test a variety of values. In the process of conducting these withdrawals and deposits, we will pause and check that the account balance matches what it should be based on our transactions. If we find a bug in any of these features, we will look for another case that produces a similar error to confirm the bug and locate it, and then discontinue testing on the feature. We will stop the testing because any trial amount will likely be incorrect. 

**Testing Pair #2: Lauraine and Rachel’s Plan:**
Our exploratory plan includes testing the services the ATM must be able to provide to the customer outlined in Appendix B.1. The key features outlined are:
A customer must be able to make a cash withdrawal from any suitable account linked to the card, in multiples of $20.00. Approval must be obtained from the bank before cash is dispensed.
A customer must be able to make a deposit to any account linked to the card, consisting of cash and/or checks in an envelope. The customer will enter the amount of the deposit into the ATM, subject to manual verification when the envelope is removed from the machine by an operator. Approval must be obtained from the bank before physically accepting the envelope. 
A customer must be able to make a transfer of money between any two accounts linked to the card. 
A customer must be able to make a balance inquiry of any account linked to the card. 
A customer must be able to abort a transaction in progress by pressing the Cancel key instead of responding to a request from the machine.

*Feature 1 Tests:*
To test this feature, we will first see the funds in each account and then attempt to withdraw appropriate money in multiples of $20 (40, 60). Each time we withdraw money, we will ensure that the balance is correctly reflected. To test a feature that should fail, we will attempt to withdraw more money than what is available in the account to ensure an appropriate error message is displayed and no money is withdrawn. Again, we will ensure that the balance is properly reflected on the screen.

*Feature 2 Tests:*
We will attempt to deposit money into the account. First, we will try $0.01 then $10; which should be correctly reflected correctly on the screen.

*Feature 3 Test:*
To test this feature, we will try to transfer the money from and/or to an account that is not linked to the card. For card 1, we will try to transfer $20 from their checkings account to their money market account. This should not be possible because this card does not have a money market account linked to it. To test if the feature works as attended, with the same card, we will be transferring $20 from their savings account to their checking account.

*Feature 4 Test:*
We will check the balance inquiry of all accounts and compare them to the actual balances.

*Feature 5 Test:*
During each type of transaction, we will click cancel to ensure this feature correctly cancels the operation. We will be clicking cancel at different times during the transaction to make sure that a user is able to abort at any given moment.


# Comparison of exploratory and manual functional testing

Comparing the exploratory testing of the two pairs, we noticed that there were many similarities between the issues that both pairs discovered. Because of the change we got to split into pairs, we were all able to review all of our issues with a fresh perspective which allowed for a better review once completed. When comparing both exploratory plans, we also noticed some differences between both pairs. For example, pair 1 thought of testing the pin numbers and their link to the correct card while pair 2 thought of testing transferring money from and/or to an account that is not linked to the card. This type of diverse thinking is what allowed us to find as many issues as we did. With the manual functional testing, we split up all 40 tests between the four of us, which was a more efficient approach. After, we were able to review each other's issues and analyze them to make sure they were reliable and made sense. 

# Notes and discussion of the peer reviews of defect reports

When we reviewed the other partnership’s defect report, we found many similarities between our test cases. For example, both of our pairings had tested both withdrawal and deposit transactions. This is most likely because the two operations make up some of the basic ATM functionalities, and the results need to be accurate in a real-world application. Another similarity is that everyone’s defect reports were easy to follow and replicate when we redid our testing. This was extremely beneficial because it allowed us to find the errors faster. Although there were many similarities, there were also a few differences. First off, the amount of money we tested for withdrawals and deposits was different in our test cases. This helped us identify some of the mathematical errors with the program. Secondly, some of the program errors that occurred when arriving at certain outputs were not recorded by each team. This could be due to the fact that one of the pairs finished their test cases before the other pair, and therefore the second pair noted that the issue was already recorded, or simply because some of the test cases had many errors such as the various parts of the receipt that were printed at the end of some transactions. It was easy to miss a small spelling mistake, or in my pair’s case realizing during our second round of testing that the transfer feature had flipped around the accounts and the account that the money was being moved from was instead being the one that the funds were being moved to, and vice versa. Overall, having two different defect reports helped us to notice details that the other team had missed, and thus provide a more accurate set of test cases.

# How the pair testing was managed and team work/effort was divided 
Our team used Discord to communicate for Assignment 1. Since the class list is fluctuating, groups were not given official group numbers. We weren’t assigned a group number before joining the lab session at 11 AM on January 20th - hence *the group document with our names was submitted with an unofficial number of our choosing (group 22)*. 

We proceeded to work in pairs for the Exploratory testing with the team divided into two pairs: 
- Pair 1 with Alexis and Abhay
- Pair 2 with Rachel and Lauraine
The work divided in the first testing was with Partner 1 (the Tester) sharing their screen with version 1.0 of the ATM project and Partner 2 (the Developer) was creating the issues in the Backlog system with the correct information being reported (also screen sharing with Partner 1). 

For the manual scripted testing, we regrouped and split up the defects numerically and divided them equally. Each of us recorded any bugs we found in Backlog and assigned them a version number of 1.0 since this is the software we were testing on. When the time came to do the regression testing on version 1.1, we each checked the same 10 cases we explored from the manual scripted testing to see if the issue still persisted or not. If the issue was cleared or continued to persist, the tester would mark it accordingly. If the issue was new, the tester would add it into Backlog with the version 1.1 label. Anyone who finished their test cases early would help the others finish their last test. Once the tests were all written into Backlog, we all reviewed them to ensure consistency among the descriptions. The effort for the report was also a combination of our time with each member picking up multiple sections to write this document completely. 


# Difficulties encountered, challenges overcome, and lessons learned

When first using the ATM System, it was a slow start since the system was new to us. With more practice navigating the system through applying the tests, it got much easier to navigate. Initially, we were a little unsure about the purpose and use of Backlog. We were unsure if the entries were relevant to the defects that we needed to look for or not, but with more instruction as time proceeded, we had a clear understanding of the purpose and meaning of these entries. A lesson we learned was the importance of versioning in applications. It is critical to document the versions of an application where a bug occurred and if/when it was resolved. Continuous maintainability is essential to ensure documentation details the current working features of an application. 

# Comments/feedback on the lab and lab document itself

The lab session itself felt a bit disorganized. We all felt quite lost and did not have any clue at the beginning of what we were supposed to do. The lab documents felt overwhelming at first but as we started working through them and asking questions in the lab session, it started to make more sense what we had to accomplish. The lab document, at some times, was quite vague in its instructions, which made us unsure of how to proceed with the assigned tasks. This was resolved within our group members by reaching a clear conclusion on how to interpret the lab assignment to the best of our knowledge. Using the GitHub Classroom feature was a nice addition to the labs as it allows each member in the group to get more familiarized with Git as in the industry, Git is starting to become the dominant tool that companies use. Familiarizing ourselves with Git as a student is a good practice for the workplace. Moreover, since we are all collaborating on this lab, it makes it easier to keep track of any file changes. Later labs, when we start writing our own test cases in JUnit, it will become smoother. 

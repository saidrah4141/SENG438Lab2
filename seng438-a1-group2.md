>   **SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: Group Number      |
|-----------------|
| Said Rahmani                |   
| Qasim Amar              |   
| Ahmed Addullah              |   
| Muhammad Bilal             |   


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

In this lab we were given two versions of an ATM system and tested the system using exploratory, manual scripted testing, and regression testing. Initially we had to spend 30 minutes to perform an exploratory test where the tester is given the ability to freely explore the program and learn the system and unocover ant unexpected issues that aren't always found in the scripted testing. What we learned about exploratory testing is understanding the requirment of the program then creating tests based on that. We created high level test plan to guide our exploratory testing. After completing the exploratory testing phases and reporting any bugs we encountered we moved onto the manual scripting tests. We foud manual testing more structered and it was explicit in what the expected outcomes were. The manual scripted tests were provided to us and we found it easier than exploratory because it was more detailed and it ensured to test if all software specifications were functional. Lastly we performed regression testing on the newest version next version of the software,1.1, the prior being 1.0. The regression testing allowed us to check if the bugs in the previous versions were fixed and if there were any new unexpected bugs.  

# High-level description of the exploratory testing plan

Test Plan #1 Qasim and Said:

High Level test plan: 
Our plan is to create a test for each feature outlined in Appendix B. We will have tests that ensure that a feature works correctly and will attempt to test edge cases as well:

Feature 1: A customer must be able to make a cash withdrawal from any suitable account
    linked to the card, in multiples of $20.00. Approval must be obtained from the bank before cash is dispensed.

Test 1.1: Attempt to make a withdrawal from every account available within the available limit of money available in the account

Test1.2 Attempt to make a withdrawal from every account above the limit available

Feature 2: A customer must be able to make a deposit to any account linked to the card, consisting of cash and/or checks in an envelope. The customer will enter the amount of the deposit into the ATM, subject to manual verification when the envelope is removed from the machine by an operator. Approval must be obtained from the bank before physically accepting the envelope.

Test 2.1: Make a deposit into each account and manually confirm the total amounts are correct after a deposit. 

Feature 3 and 4: A customer must be able to make a transfer of money between any two accounts linked to the card.  A customer must be able to make a balance inquiry of any account linked to the card.

Test 3.1: Ensure the balance can be viewed for each account. 

Test 3.2: Make a transfer between every account and manually check the balance of each account after atransfer to ensure money was correctly withdrawn from one account to another

Feature 5: A customer must be able to abort a transaction in progress by pressing the Cancel key instead of responding to a request from the machine.


Test 5.1: Attempt to abort a withdrawal request from every account

Test 5.2: Attempt to abort a deposit request from every account

Test 5.3: Attempt to abort a transfer request from every account

Feature 6: The ATM will communicate each transaction to the bank and obtain verification
that it was allowed by the bank. Ordinarily, a transaction will be considered
complete by the bank once it has been approved. In the case of a deposit, a
second message will be sent to the bank indicating that the customer has
deposited the envelope. (If the customer fails to deposit the envelope within
the timeout period, or presses cancel instead, no second message will be sent to
the bank and the deposit will not be credited to the customer.)

Test 6.1: Attempt to make a deposit and do not enter an envelope wait until you receive a timeout error/message. 

Feature 7: If the bank determines that the customer's PIN is invalid, the customer will be
required to re-enter the PIN before a transaction can proceed. If the customer
is unable to successfully enter the PIN after three tries, the card will be
permanently retained by the machine, and the customer will have to contact the
bank to get it back.

Test 7.1: Enter an incorrect pin 3 times in a row to check if the machine will hold the card

Feature 8: The ATM will have a key-operated switch that will allow an operator to start and
stop the servicing of customers. After turning the switch to the "on" position,
the operator will be required to verify and enter the total cash on hand. The
machine can only be turned off when it is not servicing a customer. When the
switch is moved to the "off" position, the machine will shut down, so that the
operator may remove deposit envelopes and reload the machine with cash, blank
receipts, etc.

Test 8.1: Try to turn off the machine while in progress of serviving a customer

Test Plan #2 Ahmed and Bilal:

Our plan for exploratory testing was for each of us to test one of the cards, testing all the functions related to deposit, withdrawal, transfer, and inquiry for that card. We made sure to test the most common paths and the exceptional paths as well as analyze the output at each step and compare it to the expected outputs. Once we completed testing at the card level, we compared and recorded our findings and then proceeded to test the system as a whole by entering incorrect pins, card numbers, insufficient atm balance, and every other possible case where something could go wrong. We used the driver navigator pair programming approach to test the system as a whole. Lastly, we conducted one final test at the card level by entering insufficient atm funds and retesting the withdrawal function for both cards.



# Comparison of exploratory and manual functional testing
Exploratory testing isn't very structured you have an idea of what you are testing based on the requirments but it is not as detailed as manual scripted testing. It reflects how creative the tester is and how they try to uncover bugs in the program. When the two pairs in our group completed the exploratory testing we were able to compare our findings and gain new perspective and see if one group missed something. 

Manual Functionl Testing is when a tester manually tests the software based on its requiremnets and promised functionalities. The tester is given a deatiled testing plan which covers all apects of the required funcitonality. It has different test cases for each functionality ie. withdrawl, deposit, trasnfer, inquiry, and security.The test suite provided is very clear and rigid and outlines what the expected outcome should be based on a sequncee of steps. The test suite provided to us in appendix c had 40 test which were split amongst the group. After each member completed the test we dicussed each test case to ensure it was performed correctly and ensured a bug was reported correctly. 

# Notes and discussion of the peer reviews of defect reports
For our defect reports we decided to use Azure DevOps. When finding any bugs we added them with detailed descriptions on how to recreate it, tags that described the type of testing the bug was found from, and the version of the program.

Upon the completion of the exploratory testing we found around 13 bugs combined between the two pairs. Which we then reported in Azure DevOps with detailed recreation steps and expected outcomes compared to actual outcomes. We also included tags for each reports specify if it was also found from manual scripted testing and the version of the software in which it was present. 

After completing regression testing we found most the bugs to be resolved and adjusted the states withing the bug report accordingly.


# How the pair testing was managed and team work/effort was divided 

Pair #1 (Said & Qasim)

Pair #2 (Bilal & Ahmed)

During the explaratory testing stage, both pairs came up with a testing plan to execute. Upon completion and after finding bugs we compared our findings between the pairs and worked together to report them into Azure DevOps.

For the manual scripted testing we came together to executed each test case and report our findings. We took turns between performing the tests and keeping track of what has been done.

Finally for regression testing we split the bugs we found between each memeber and performed testing on the updated software. 


# Difficulties encountered, challenges overcome, and lessons learned
In the begining we were confused how to properly report bugs and specific information we should include when reporting bugs. And the system was a little confusing at first to use. But as we spent more time playing around with it it was a lot easier to navigate. We also learned the importance of testing and bug reoprting. Specifically with detailed reoprts such as including the version how to recreate the bug and discussing it with other members. We leanred how intriquite the porcess can be and how documentation is very important. 

# Comments/feedback on the lab and lab document itself

At the start the lab felt pretty challenging due to finding certain parts of the instructions unclear. Since it was our first time doing a lab like this it took some time to full understand. However from the TA's assistance and building familiarity with the taks it became easier to complete as required.

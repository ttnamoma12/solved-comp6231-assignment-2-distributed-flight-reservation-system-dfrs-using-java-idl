Download Link: https://assignmentchef.com/product/solved-comp6231-assignment-2-distributed-flight-reservation-system-dfrs-using-java-idl
<br>
In this assignment, you are going to implement the Distributed Flight Reservation System (DFRS) from Assignment 1 in CORBA using Java IDL. In addition to the 3 operations in Assignment 1 (namely, <em>bookFlight</em>, <em>getBookedFlightCount</em>, and <em>editFlightRecord</em>) the following operation also needs to be implemented.

<ul>

 <li><em>transferReservation </em>(<em>PassengerID</em>, <em>CurrentCity</em>, <em>OtherCity</em>)</li>

</ul>

This function is used by a manager (<em>ManagerID</em>) to transfer a previously made flight reservation i.e. passenger record (<em>PassengerID</em>) from the <em>CurrentCity </em>to the <em>OtherCity</em>. When a manager invokes this method through a <em>MangerClient </em>program, the server associated with the <em>CurrentCity </em>checks whether the passenger (<em>PassengerID</em>) has the specified flight reservation on it and then transfers the reservation with same details to the <em>OtherCity, </em>using UDP/IP messages (instead of invoking the <em>bookFlight </em>function at the other server). Note that creating the required reservation at the <em>OtherCity </em>and cancelling the existing reservation at the <em>CurrentCity </em>should be done atomically (that is, both should be done or none should be done) using UDP/IP messages.

In this assignment you are going to develop this modified DFRS application in CORBA using Java IDL. Specifically, do the following:

<ul>

 <li>Write the Java IDL interface definition for the modified DFRS with all the 4 specified operations.</li>

 <li>Implement the modified DFRS in CORBA. You should design a server that maximizes concurrency. In other words, use proper synchronization that allows multiple officers to perform operations for the same or different records at the same time.</li>

 <li>Test your application by running multiple clients (Passengers and Managers) with the 3 servers. Your test cases should check correct concurrent access of shared data, and the atomicity of <em>transferReservation</em></li>

</ul>




Your submission will be graded for correct and efficient implementation of the <em>transferReservation</em> operation in addition to correct use and implementation of mutual exclusion in accessing shared data and proper exploitation of concurrency to achieve high performance.

<strong> </strong>

<em>COMP 6231</em> <em> (Distributed System Design), Fall 2016 — Assignment 2                                        Page 2</em>

<strong>Marking Scheme </strong>

<strong>[30%]</strong>  <em>Design Documentation</em>: Describe the techniques you use and your architecture, including the data structures. Design proper and sufficient test scenarios and explain what you want to test. Describe the most important/difficult part in this assignment. You can use UML and text description, but limit the document to 10 pages. Submit the documentation and code by the due date; print the documentation and bring it to your demo.

<strong>[70%]</strong>  <em>Demo in the Lab</em>: You have to register for a 5-minute demo. Please come to the lab session and choose your preferred demo time in advance. You cannot demo without registering, so if you did not register before the demo week, you will lose  40% of the marks. Your demo should focus on the following.

[50%] C<em>orrectness of code:</em> Demo your designed test scenarios to illustrate the correctness of your design. If your test scenarios do not cover all possible issues, you’ll lose part of mark up to 40%. You will also be evaluated on                        the implementation of your design.

[20%] <em>Questions:</em> You need to answer some simple questions (like what we’ve discussed during lab tutorials) during the demo. They can be theoretical related directly to your implementation of the assignment.




<strong>Questions </strong>

If you are having difficulties understanding sections of this assignment, feel free to email the Teaching Assistant Mr. Harpreet Narula at <u><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="264e47545654434352484754534a4716161366414b474f4a0845494b">[email protected]</a></u>. It is strongly recommended that you attend the tutorial sessions which will cover various aspects of the assignment.

<strong> </strong>
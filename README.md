# LMSAssesment(VERIPARK)
Simple Library Management System
1 Important
Please make sure you read the entire document before you begin with the assignment. The document
below contains following sections -
1. Overview - explains the existing functionality.
2. Security - the created user name and password.
3. Requirements - your assignment that we request you to undertake.
Output is one part of evaluation. We look forward to seeing good coding practice. Also, we expect your
understanding of code, architecture, etc. if you use any internet resource.
Good luck on your assignment ��
2 Overview
Consider this a Library Management application. It contains Books and Customers records. A customer
can borrow books from the Library and then return it. Other customers can borrow a returned book. If a
customer borrows a book, he must return it within 14 working days; otherwise, he has to pay a penalty
of 5 AED for every additional working day. Currently, a working day is considered a day which is not a
Saturday and which is not a Sunday.
Following is the current system
2.1 Books

Book records can be Added, Edited &amp; Viewed details of. No need of ‘DELETE’ action. A book
can also be borrowed by Customer. The Book Module contains following fields -
1. Title
2. ISBN
3. Author
4. Publisher
2.2 Customers

Customer records can be Added, Viewed details of, Edited and Deleted. While Adding,
Editing and Viewing Customer, the following fields are involved -
1. Name
2. Address
3. Contact
4. National ID
A Borrowal History table is also displayed in Customer Detail page which displays all the
Books this Customer has borrowed in past.

2.3 Security

There are two users that can login to this application
1. librarian@veripark.test
2. supervisor@veripark.test
3. Password for both - Password1$

3 New Requirement
4.1. You are requested to create and implement a new (MVC) module - &quot;BusinessHoliday&quot;. A
Business Holiday would be one day or more days in a sequence. The Business Holiday module
should display the fields as in below table.
Note: These are only Display Names, you may name the fields in Code / Database according to
regular coding standards.
#
Display
Name Description Business Rules

a.
Holiday
Occasion

This is a caption of the Holiday for
understanding.

● Mandatory field
● Maximum 10 characters
● Should begin with Text of upper case

b. From Date

The date from which this Holiday
begins. This date is inclusive of
Holiday.

● Hint:In some version of Chrome, value isn&#39;t
displayed in Edit Mode for
&quot;DataType.Date.&quot; Thus select appropriate
formatstring.
● Mandatory field

c. To Date The date till which this Holiday is
valid. This date is inclusive of Holiday.

● Mandatory field
● Same as &#39;From Date&#39; if it is One Day
holiday
● if only one holiday, the From Date and To
Date would be the same.

d. Active ?

If IsActive=True / Yes, this Holiday
should not be considered as a
Business Day or a Working Day.
Or, in other words, while doing
Business Day calculation, logic should
not count these days in calculation
just like we should not count
weekends.

●

Default value should be Active / Yes / True

4.2. Kindly ensure to seed 5 holidays in the upcoming 30 days so that we don&#39;t have to run SQL
statements while testing your code.

4.3. Please create a page for displaying a list of Business Holidays with following fields
4.3.1. Holiday Occasion
4.3.2. From Date
4.3.3. To Date
4.3.4. Active ?
4.3.5. Action – Display links to Edit and Delete the Business Holiday.
Important: If any change is made to existing Holiday dates or if new Holidays are defined,
you do not have to recalculate any calculated values already existing in the database.
4.4. Business Holidays should be now used while calculation of
4.4.1. Penalty Amount if the Book is Returned later than Required Return Date.
4.4.2. Book return date while borrowing book.
4.5. Ensure to display the title of the Book in the Borrowal History section of Customer Details.
4.6. Currently, the same borrow history is displayed in all customer&#39;s detail pages. Pl check why and
make necessary corrections.
4.7. Currently there is no Authorization implemented and all pages and actions are accessible to
Anonymous users. Pl implement below authorization.
4.7.1. The user librarian@veripark.test (or other users who have this same role) should be
able to
4.7.1.1. Borrow &amp; Return books
4.7.1.2. View Book details
4.7.1.3. See Borrowal History
4.7.1.4. View List and Details of Customers and Books
4.7.2. The user supervisor@veripark.test (or other users who have this same role) should be
able to
4.7.2.1. do all the tasks librarian@veripark.test has permission to
4.7.2.2. Add, Edit and Delete Books, Customers and Business Holidays
4.7.3. No Authorization be needed for Viewing Book List or Details

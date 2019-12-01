# Fever 

# Overview
This is a simple report based on one loyalty program implemented on October 1st. The provided dataset contains six key variables (date_purchased, id_ticket, id_user, city_of_event, revenue and is_free_ticket) and 382277 purchase records of 80199 users from 2019-08-01 to 2019-11-01. 

# Research Question
We focus on 1) users' purchase behaviour (pay for ticket or not) 2)the most valuable user and 3)an overall performance of this program.

# Data Preparation 
We started with data prepartion process. We first removed 4 missing values, then transformed Date into Weekdays/Month, for better presenting revenue and ticket sales by timelines. 
Besides, we noticed that, 48478 users started their first purcahse before Oct 1st, however, approximate 80% (38927 out of 48478) stop using Fever after October 1st, therefore,we removed them from the current dataset directly. For the rest 9551 regular users, we comapred them with 31721 new users who first buy after October. We assume the difference in consumption behavior between regular users and new users are mainly determained by the loylaty program. 

# Date Reviewing 
In the last three months:
* Fever released over 331400 free tickets to users and only 50875 paid ticket.
* Approximate 40% regular users and 26.2% new users 'purchased' free tickets only.
* For regular users, the paid tickets take 5.7% of all sold tickets in August and Sepetember, while the Paid ticket rate increased to 9% in October. For new users, over 46.6% paid ticket ratio gives a very promising perspetive of revenues.
* Indeed, the line chart showed how revenues change. Total Revenues in October is about 888,251 USD, 201,484 USD (22.8%) comes from regular users and 686,767 USD (77.3%) comes from new users; 
* When do they buy? We answered this question by grouping tickets sales by Weekdays. Not surprising, Weekends are the peak days, but worth to notice that, new users love buying tickets from Fever every singel day! 
* Who buy most and who pay most? User_id 42702677 spent 4184 USD purchased 110 tickets (0 free) in last three month, we could consider this as a valued shared account. Besdies that, User_id 44177513 spent 616 USD on 28 paid ticket in October, top 1 among all New users. The other new user, User_id 44200840 spent 1893 USD on 23 tickets, also becasue of this, we created a new variable id_revenue to measure ID's revenue. We not only care who buy more, but importantly, who Pay more.
* There are two event cities in this dataset, we believe City 6 is either a new market for Fever or a smaller city with much smaller population. Over 360,000 tickets are sold/free sent in City 5 while 13740 in City 6. Majority of regular users used free tickets in City 5, while the bright furture is coming. We can see the ticket payment structure is changing dramatically after New users flow in. Fewer free tickets and increasing revenue, excellent!

# Conclusion and Limitation
* The p-value of id_revenue is much smaller than 0.05, which give us a signal that this loyalty program effects id_revenue significantly. 
* We may lack of information about the cost of running this program, the cost of releasing free tickets, with those information, we may combine two strategies to maximize the revenues whilst reducing the costs.
* We did not work much on those regular users who left Fever after Oct, but we assume if we compare them with other regular users who stayed, we may find out the reasones. Also, other information such as user feedbacks, purchased products will be useful, too, we will never worry about no stories to tell!

# Hospitality-Sales

AtliQ Grands owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands are losing its market share and revenue in the luxury/business hotel category. As a strategic move, the managing director of AtliQ Grands wanted to incorporate “Business and Data Intelligence” to regain market share and revenue
Task:
Create the metrics according to the metric list.
Create a dashboard according to the mock-up provided by stakeholders.
Create relevant insights that are not provided in the metric list/mock-up dashboard.

#KPI's Matrices:-

ADR Calculate the ADR(Average Daily rate) - It is the ratio of revenue to the total rooms booked/sold. It is the measure of the average paid for rooms sold in a given time period.
Realisation % calculate the realisation percentage. It is nothing but the successful "checked out" percentage over all bookings happened.
RevPAR Calculate the RevPAR(Revenue Per Available Room)RevPAR represents the revenue generated per available room, whether or not they are occupied. RevPAR helps hotels measure their revenue generating performance to accurately price rooms. RevPAR can help hotels measure themselves against other properties or brands.
RevPAR = DIVIDE([Revenue],[Total Capacity])
 4.DBRN calculate DBRN(Daily Booked Room Nights) This metrics tells on average how many rooms are booked for a day considering a time period.
DBRN = DIVIDE([Total Bookings], [No of days])
5. DBRN calculate DBRN(Daily Booked Room Nights)

 This metrics tells on average how many rooms are booked for a day considering a time period

 DBRN = DIVIDE([Total Bookings], [No of days])

6. DSRN calculate DSRN(Daily Sellable Room Nights)

 This metrics tells on average how many rooms are ready to sell for a day considering a time period

 DSRN = DIVIDE([Total Capacity], [No of days]) 

7.DURN calculate DURN(Daily Utilized Room Nights)
This metric tells on average how many rooms are successfully utilized by customers for a day considering a time period
 DURN = DIVIDE([Total Checked Out],[No of days]) 

8. Revenue WoW change % To get the revenue change percentage week over week.

 Here, 
 revcw for current week
 revpw for previous week
 Revenue WoW change % = 
 Var selv = IF(HASONEFILTER(dim_date[wn]),SELECTEDVALUE(dim_date[wn]),MAX(dim_date[wn]))
 var revcw = CALCULATE([Revenue],dim_date[wn]= selv)
 var revpw = CALCULATE([Revenue],FILTER(ALL(dim_date),dim_date[wn]= selv-1))

 return
 DIVIDE(revcw,revpw,0)-1

9. Occupancy WoW change % To get the occupancy change percentage week over week.

 Here, 
 revcw for current week
 revpw for previous week Occupancy WoW change % = 
 Var selv = IF(HASONEFILTER(dim_date[wn]),SELECTEDVALUE(dim_date[wn]),MAX(dim_date[wn]))
 var revcw = CALCULATE([Occupancy %],dim_date[wn]= selv)
 var revpw = CALCULATE([Occupancy %],FILTER(ALL(dim_date),dim_date[wn]= selv-1))

 return
DIVIDE(revcw,revpw,0)-1

10. ADR WoW change % To get the ADR(Average Daily rate) change percentage week over week.

 Here, 
 revcw for current week
 revpw for previous week ADR WoW change % = 
 Var selv = IF(HASONEFILTER(dim_date[wn]),SELECTEDVALUE(dim_date[wn]),MAX(dim_date[wn]))
 var revcw = CALCULATE([ADR],dim_date[wn]= selv)
 var revpw = CALCULATE([ADR],FILTER(ALL(dim_date),dim_date[wn]= selv-1))

 return
DIVIDE(revcw,revpw,0)-1

11. Revpar WoW change % To get the RevPar(Revenue Per Available Room) change percentage week over week.

 Here, 
 revcw for current week
 revpw for previous week Revpar WoW change % = 
 Var selv = IF(HASONEFILTER(dim_date[wn]),SELECTEDVALUE(dim_date[wn]),MAX(dim_date[wn]))
 var revcw = CALCULATE([RevPAR],dim_date[wn]= selv)
 var revpw = CALCULATE([RevPAR],FILTER(ALL(dim_date),dim_date[wn]= selv-1))

 return
DIVIDE(revcw,revpw,0)-1

12. Realisation WoW change % To get the Realisation change percentage week over week.

 Here, 
 revcw for current week
 revpw for previous week Realisation WoW change % = 
 Var selv = IF(HASONEFILTER(dim_date[wn]),SELECTEDVALUE(dim_date[wn]),MAX(dim_date[wn]))
 var revcw = CALCULATE([Realisation %],dim_date[wn]= selv)
 var revpw = CALCULATE([Realisation %],FILTER(ALL(dim_date),dim_date[wn]= selv-1))

 return
 DIVIDE(revcw,revpw,0)-1

13. DSRN WoW change % To get the DSRN(Daily Sellable Room Nights) change percentage week over week.

 Here, 
 revcw for current week
 revpw for previous week DSRN WoW change % = 
 Var selv = IF(HASONEFILTER(dim_date[wn]),SELECTEDVALUE(dim_date[wn]),MAX(dim_date[wn]))
 var revcw = CALCULATE([DSRN],dim_date[wn]= selv)
 var revpw = CALCULATE([DSRN],FILTER(ALL(dim_date),dim_date[wn]= selv-1))

 return
 DIVIDE(revcw,revpw,0)-1


#Insights:-

At first, we can compare the price rates between weekdays and weekends, and we can see that there is no significant difference in price.
Most of the revenue is coming from the luxury category and Atilq Exotica.
Occupancy is similar in both categories.
Mumbai has the highest number of bookings, but in terms of revenue, Bangalore is generating more revenue.
In the trend matrices of months and weeks, in the month of July, the last week's occupancy was lower compared to other weeks of the month.

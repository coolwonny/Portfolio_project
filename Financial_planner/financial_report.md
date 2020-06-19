# Financial Report

---
       
       

## Budget Analysis
---

From the Plaid transactions data for the past 90 days from now, we sorted out 6 different spending categories and aggregated spendings in the same categories as shown in the table below.   

![Total Expenses per category](Images\expense_groupby_category.png)

From the Plaid transactions data for the past 90 days from now, we sorted out 6 different spending categories and aggregated spendings in the same categories as shown in the table below.
![Total Expenses per category](expense groupby category.png)

Also, we plotted it in a pie chart.    

![Spending Categories Pie Chart](Images\pie_chart_new.png)

As shown, 'Transfer' takes the overwhelming part of total expenses followed by 'Payment' and 'Food & Drink'. Transfer has two major transactions, ACH Electronic Credit($17.5K) and CD Deposit($3K) while Payment does automatic payments ($6.2K).
This is tricky part of the analysis because ACH transfers are likely seen as incomes. However, we do not know whether it is income or not as we cannot rule out the possibility of ACHs being other expenses such as salary payout, we determined to regard it as expenses.

Next, we grouped the expenses data into each month. Surprisingly we had the exact same values in each and every month at $10.6K.    

![Monthly expenses](Images\Monthly_spending.png)    

Also, we plotted in a bar chart.    

![Monthly spending bar chart](Images\bar_chart.png)

Regardless of the accuracy of data provided, the monthly spending has been absolutely stable and each category shows exactly the same patterns over the 3 months period.

On the other hand, the data returned previous annual income, monthly income and projected annual income. According to them, monthly income is $0.5K and annual gross income was $7.3K last year and would be $7.4K for the coming year. Given these and expenses for the current 90 days, the target client could be in solvency unless he do not bring more cash from other assets; the average monthly spending($10.6K) could not be covered by the monthly income($0.5K), generating monthly deficit of -$10.1K, which will bring annual deficit of $ 121K.
      
           
           
     
## Retirement Planning
---

We have simulated a retirement plan where a customer is encouraged to create a stock portfolio comprised of two stocks in which 'SPY' is a S&P500 ETF that benchmarks a stock market return whilst 'AGG' is a aggregate US bond ETF that plays like a bond. The customer would start with initial investment of USD20K which will be weighted 60:40 to 'AGG' and 'SPY', respectively.  

The strategy here is quite conservative and reasonable given the risk/return balance as a retirement plan. We need a simulation result to help the prospective customer understand how his portfolio presumably perform until his retirement. For doing this we chose to run the monte carlo simulation based on the stocks' historical data(Y2019) , calculated the average mean and standard deviation during that year and assumed the future price change would be normally distributed over the entire projection period. 

We ran the monte carlo simulation 500 times for 30 years.     

![500 Simulation of Cumulative Portfolio Return Trajectories over the next 30 years](Images\500_simulations_cumulative_return.png)

From the above, we can see that the graphs are almost flat until 10 years after which the range or band becomes soaring to the end that comes in the next 30 years. In the next bar chart showing the distribution of the ending day return(after 30 years), we can figure out the portfolio returns would be between 3700% and 9100%, given 90% confidence interval.   

![Distribution of the ending returns](Images\distribution_histogram.png)

 This massive return is attributed to the bullish stock market in 2019 that was used for our historical return and risk. Notwithstanding the rosy conjecture, we strongly recommend using more historical data - longer time span or including the current market anomaly due to pandemic - to get more trimmed projection.

As a result, we could get the expected returns at 30 years. 10th percentile is 40.2(or 4020%), 50th percentile at 58.9 and 90th percentile at 82.9. To put this another way, if the customer put a $20,000 initial investment in the portfolio now, he could expect a dollar return of $804K for 10th percentile chance from bottom, $1178K for 50% chance and $1659K for 90th percentile.      

![5th, 50th and 95th quartiles of the cumulative returns over time](Images\quantiles.png)

Given the current projected annual income of $6085 from the Plaid analysis, we assumed a 4% withdraw rate from the retirement portfolio. This can be met when his portfolio dollar return would be equal or greater than $152K (= 6085 / 4% ). As mentioned above, he would get $804K after 30 years as a 10th percentile, we can say he might have a 90% chance of the expected returns will be greater than $804K. In additon, if he increased the initial investment by 50% or $10K, which not necessarily required in this scenario, he could have more return on investment.



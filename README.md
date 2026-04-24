\# Delivery Operations Optimization



I'm a CSE undergrad transitioning into operations and strategy.  

I built this project to teach myself how to think like an operations analyst starting with a question I genuinely wanted to answer:



\*\*Where does time actually get lost in a food delivery?\*\*



Not assumptions. Not theory. I wanted to see it directly in data.



\---



So I created a dataset of 250 delivery orders from scratch, modeled on how platforms like Swiggy and Zomato operate prep times, rider assignment, pickup delays, transit time, traffic, failures, everything. Then I broke down every minute of the delivery journey to identify where things actually slow down.



Here’s what came out of it.



\---



\*\*Finding 1: Transit is eating more than half the delivery\*\*



Average delivery time is 57 minutes. Out of that, 32.3 minutes is just the rider in transit—that’s 56% of the total journey.  

Prep, waiting, and pickup delays together make up the remaining 25 minutes.



!\[Time Phase Breakdown](images/chart\_01\_time\_phase\_breakdown.png)



\---



\*\*Finding 2: Peak hours add 10% to delivery time\*\*



Peak hour orders (lunch and dinner windows) average 59.6 minutes, compared to 54.1 minutes off-peak.  

The key issue isn’t just traffic-rider availability drops from 16.4 to 13.7 while order volume increases.  

More demand, fewer riders, longer delays.



!\[Peak vs Off-Peak](images/chart\_02\_peak\_vs\_offpeak.png)



\---



\*\*Finding 3: Bulk orders take 41% longer, and it’s entirely the kitchen\*\*



Bulk orders take 32 minutes to prepare, while normal orders take 15.3 minutes.  

Transit time is almost the same for both.  



This makes it clear that the delay isn’t on the road, it’s in the kitchen struggling to handle larger, more complex orders.



!\[Normal vs Bulk](images/chart\_03\_normal\_vs\_bulk.png)



\---



\*\*Finding 4: Distance matters more than traffic\*\*



This one was unexpected.  

Orders marked as high traffic actually showed lower transit time than medium traffic orders.  



Looking deeper, high traffic orders tend to be shorter distances (3.9 km vs 4.8 km).  

So distance ends up being a stronger driver of delivery time than traffic itself.



!\[Traffic Impact](images/chart\_04\_traffic\_impact.png)



\---



\*\*Finding 5: Most failures happen before peak hours\*\*



The 4-6 PM window shows the highest failure rate at 9.1%.  

Not late evening. Not peak dinner.  



This suggests kitchens are already getting overloaded before peak demand fully hits, causing failures early in the pipeline.



!\[Failure by Time Slot](images/chart\_05\_failure\_by\_timeslot.png)



\---



\*\*Finding 6: Huge variation in rider performance\*\*



R14 averages 22.6 minutes in transit.  

R11 averages 38.2 minutes.  



That’s a 15.6-minute gap within the same system.  

This level of variation points to issues in routing, monitoring, or rider allocation.



!\[Rider Performance](images/chart\_06\_rider\_performance.png)



\---



\*\*Finding 7: 7 PM is the system’s breaking point\*\*



At hour 19 (7 PM), there are 35 orders with only 9.9 riders available, the lowest supply level.  

Delivery time spikes to 63.5 minutes.  



This is a clear demand-supply mismatch happening at the worst possible time.



!\[Hourly Volume](images/chart\_07\_hourly\_volume.png)



\---



\*\*Finding 8: Short distance doesn’t mean fast delivery\*\*



Orders under 2 km still take around 43 minutes on average.  

Transit only accounts for 17.5 minutes.  



The remaining 26 minutes come from prep and waiting time.  

So reducing distance alone won’t fix delays.



!\[Distance Bucket](images/chart\_08\_distance\_bucket.png)



\---



\*\*What I’d fix first\*\*



Increase rider availability between 5:30-8:30 PM to address the peak hour supply gap.  

Introduce kitchen SLA alerts for bulk orders to reduce rider waiting time.  

Track and improve low-performing riders, the gap between R11 and R14 is too large.  

Pre-assign riders during evening hours to reduce idle waiting before pickup.



These recommendations come directly from what the data shows.



\---



\*\*Limitations\*\*



This is a simulated dataset, not real platform data.  

No variables for cuisine type, GPS routing, or weather.  

Hour 20 contains only one order, so it’s not reliable.  

Rider performance differences may partly reflect route allocation rather than individual efficiency.



\---



\*\*Tools\*\*



Excel for dataset creation, analysis, KPIs, and dashboards.  

GitHub for version control.



\---



\*\*About\*\*



CSE undergrad transitioning into operations and strategy.  

I like breaking systems down and figuring out where they fail.



This is my first operations project. More coming.


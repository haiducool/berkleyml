# berkleyml

LINK TO NOTEBOOK: https://github.com/haiducool/berkleyml

REPORT FOLLOWS:

Offering the right coupons at the right time can materially increase the acceptance rate, meaning they are likely more relevant for the drivers, and will be less expensive for advertisers. Historical data can be used to more accurately target the drivers, and therefore increase acceptance rate.

Before analyzing the data, I've investigated the dataset for missing and problematic data. It turned out that the column 'car' had very few observations (only 108, or <1% of total), and therefore I decided to ignore/ remove it. Then, several other columns (Bar, CoffeeHouse, etc) had missing data, however that was relatively limited (less then 2% of total observations), therefore I decided to remove those rows. The resulting dataset that was used for analysis was reduced from 12684x26 to 12079x25. 
 
The analysis focused on two subsets of the data - coupons for bars and for lower priced restaurants (<20 per meal per person). Based on the analysis performed, some of the observations :
- across all analyzed data, the average coupon acceptance rate is 57%
- acceptance rate varies greatly by coupon type, lowest is Bar with 41%, and highest is Carry out & Take away with 74%, closely followed by lower priced restaurant at 71%

BAR COUPONS:
- for bar coupons, more frequent (4~8) bar visitors were much more likely to accept coupons at 78% relative to those going to a bar less than 3 times a month, at 37% acceptance rate
- other driver attributes impacting the acceptance rate include age, whether the driver had kid passengers, their occupation, marital status. 
- some attributes are intuitive, for example whether the driver has kid passengers. Obviously as children are not allowed into a bar, the driver is not likely to accept a coupon.

LOWER PRICED RESTAURANTS COUPONS:
- for lower priced restaurant coupons, it was interesting to observe that acceptance rate was so high across whole sample at 71%, however there are important variations in rate depends on specific attributes. 
- drivers who are much more likely to accept coupons had the following attributes: destination: No urgent place, driving with friends in sunny weather at around 2 pm and 6 pm, are singly or unmarried partner, and work in protective service or construction & extraction. 
- it was interesting to observe that some attributes did not have a material impact on the rate, for example mean acceptance rate for various age groups ranged from 64% to 75%, and some like occupation had a very material impact ranging from 40% for "Building & Grounds Cleaning & Maintenance" to more than double at 89% for "Protective	Service"
- for example, coupons issued early in the morning at 7 am or last afternoon at 10 pm were much less likely to be accepted at 59% and 51% rate respectively. This is intuitive as drivers are more likely to rush to either home in the evening, or to work in the morning
- the weather during coupon issues also had a very material impact on acceptance rate with 39% for Rainy days, and 77% for Sunny days. While not surprising, it is interesting to observe that the difference in rate is close to 2x

NEXT STEPS AND RECOMMENDATIONS:
In summary, this data and analysis provided useful insights into how various attributes impact acceptance rate, and can be used in developing a predictive model to help estimate the rate for new coupons. 

I would recommend the next steps should include the following: 
1. Enriching the dataset with additional relevant attributes, for example the amount of discount offered in coupons might have an important impact. Advertisers do want customers and therefore are offering coupons, however they also want to operate a profitable business and therefore limit the amount of discount. Other useful attributes could include the impact of coupons on attracting repetitive customers, in other words to what extent coupons are a good customer acquisition strategy, vs a transactional deal.
2. Further analyzing the dataset, for example exploring the impact of distance to the bar or restaurant from the driver to further help tailer advertising programs.



Generally we knew about Data centre, 
Consider we have a Data centre and a disaster takes place out of no where leading to lose of all of our data in the data centre... shitttt this should never happen 💩

AWS solves this by having more than one data centre near in a place , which is termed as ***Availability Zone (AZ)***

*Data centres in a availability zone are synced with less latency and are high in terms of speed*

Okeyyyy Mannn, What if some natural disaster or an alien disaster👽🛸  took place and lead to the loss of data in the complete Availability zone ???? 𝌆🔥
- AWS soles this with the help of another Availability Zone which will be synced with the main AZ.... Jeeezz , this got me some relief 😮‍💨

***Thenn 😅, What the heck is an region ?***
> Regions are Geographical locations world wide where AWS hosts its data centres
> Regions in AWS are named after the location where they reside
> Regions consists of one or more availability zones

*Okayyy man ! All things clear* 🥚🐣🐥

**Now we need to select a Region for using AWS services**

To choose the right AWS region there are 4 things to consider
- Compliance [Organizations may comply regulations with regulations that the data needs to be stored in a specific geographic territory]
- Latency [Choose a region w.r.t latency as choosing an a region in US for customers in India would kill the user's state of mind with a huge latency so choosing region as India to serve customers of India has a lesser latency]
- Service Availability [All AWS services might not be available in all regions]
- Pricing[Pricing vary w.r.t region]

*Nahhh broo, what if i have global customers and I have choose my region to be US 👻*

> Here come ***Edge Locations*** ☄️ 😬
> We can consider this as an cache, where edge locations are global locations where content is cached
> considering the use case , we have a customer from India to access some resource from US region, this resource will be cached in the edge location making all the consequtive calls to be served faster





















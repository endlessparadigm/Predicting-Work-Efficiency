# Predicting-Work-Efficiency at Work
An anecdote related to a work project utilizing a Hagen-Poiseuille equation and 4-dimensional models to predict efficiency-per-team completion rate of a corporate data management project.

## Abstract
I had a really fun time as a contractor nearly 10 years ago for a major company. There was the opportunity to create an estimation of when a major data infrastructure project was to be completed. I took it upon myself to create a complex Excel spreadsheet, and apply my statistics knowledge in hopes of assiting the project management team.

> Specific details have been changed regarding the assets and topics involved given that it was a privacy related effort after all! :)

> I wrote this in a similar mindset that I had at the time, as a refreshing view of how inexperience unfolds, and when ingeniuity shows its' worth.

# The Details

It's 2014. At this point I am a simple intern with 6 months of corporate experience. I loved Excel functions, and with my ambitions looking at an analytics related career, I took it upon myself to create an Excel spreadsheet for a $6 million dollar corporate project. There were over 200 in-scope applications, 70+ databases (SQL, Oracle, mainframe and more), and more than 25 business teams involved in the effort. The expectation was to upgrade or change the infrastructure as a means of modernizing an applications' data for the entirety of IT. The project was already underway, I had access to the budget details, dev-hours logged, as well as a well-detailed existing spreadsheet of the progress or completion status of each of the assets to be modernized.

# The Challenge

The project is being very well tracked. Each of the 200+ applications have a pipeline or track for the different IT teams (such as Security, App Devs) involved for their part of the work to be completed. This was operating similar to Agile, shortly before it became more popular in today's corporate environment.

For example:

1. Onboarding (Meet with the application team, share details of the project)
2. Analysis (Review of application and application database) 
3. DEV (Upgrade of asset or asset database)
4. Security (Permissions/Protocols defined and applied)
5. Audit and Monitoring (Scheduling and automation) 
6. Signoff and onboarding (Review with business teams on the outcomes of the deliverable)

We have the dates for when an application begins or completes any of the above sections for all of the assets on the list. This was sufficient for the PM team as they can review the data and check in with a specific team regarding the status of the asset for any section listed above. 

[Screenshot as example]

# The Opportunity

As a new contractor/intern, I wanted to stand out as a competent analyst and thought we could find a way to predict the date of completion of each of all of these assets. With all of the data being gathered, I could not only predict when an asset was to be completed, but also how busy each of the teams would be at any given time (based on all of the assignments in their list, and the dates in which the planned work would fall in their bucket). 


I could then use that information as a dependency to predict the progress of subsequent applications and ideally formulate an overall project completion date! Not only that, we could even change the order of all of the work to make sure it gets completed even quicker. They'll love me definitely! Given that it was a multi-year project, I would assume it would prove useful. (It was!)

# The Complication
Having not utilized statistics in a corporate environment before (but with adequate math experience), I begin to search on how to apply predictive analytics based on existing data. One finds themselves quickly immersed in a complicated realm of wikipedia and statistics tutorials. Should I really be using these funny equations to predict when the app guy is finished setting up our folder permissions for Database XYZ?

I set off to build a spreadsheet to be used as a supplement to the tracker. This would import the start/completion dates for each of the sections. With my inexperience, I had my little mind set on determining the average completion time required for each of the work sections; such as - what is the average time it takes to onboard a new asset team to our project from the start of it at onset? 

The more I thought about it, the more complicated it became. Onboarding an app could take as little as an hour (based on our Excel dates, 1 day). When scheduling a meeting for another app, it might not be until next week Thursday that we meet (let's say 8 days from now, so 8 days effort). If I take the average, the result might be the same effort (1 hours' time) but a different elapsed time. ***head scratch*** But the actual work would still take 1 hour. How do I relate that paradigm? There is actual work or effort being done or completed, and there is the amount of time that needs to pass for completion.


# The Inexperience
At this point I am not consciously aware of the complexity of what I am now trying to accomplish. I am setting out to determine how much work each of the engineers among many others in the company are completing daily (an important metric in a still-at-waterfall world), in addition to how much time it takes for them to inform us of such work being done. Useful, right? Not only this - I could then track how the individual-not-the-team lags in relation to his or her peers, and also the delay in response to the work effort for any other team they operate with. (Example: If a security team is particularly slow with the DBA's but not with the app dev's, we could investigate this numeric animosity for even more accurate results). I'll be a manager by midnight!

> At this point, I start to be thankful for the senior engineers I worked with at the time and the patience involved on their part. :D

# The Development

After a few weeks of working on my little side project. I now had a few tables laid out featuring some neat things:

Charts and graphs!
> This included Burndown rate for different categories of apps, an overall completion date, and estimate of when the budget would run out.


Logic tables built into Excel. Not every asset requires every project step. This was asset category dependent. I took that into consideration.
> These logic tables were set up to define which section(s) are required for different assets on the tracker (asset category dependent). This way the Excel function would know what to calculate for an asset. IF(VeganDish,NoMeatCalc)


A lot of Excel functions meant for standard deviation and averages.
> Maybe soon I'll find the correct analytics to apply and get a more accurate result!

A lot of unfinished (really quite many) worksheets trying to tie everything else together.
> We'll get there soon!

A few additional ideas came to mind. Let's create a new property called DifficultyRating which we can then assign to each of the assets. This should be a one time request from the PM's, and I'm pretty familiar with a lot of these by now anyway. This property can then be utilized to affect the skew or probability of best-case/worst-case scenario of each prediction.

Time to re-think what still remains. I have averages and standard deviation applied to all assets. I have difficulty rating as a means to include a weighted average to these estimates based on the variety of applications involved. This results in a range of possible completion times for each and every asset. This means the expected completion date can be calculated for any category on the tracker. 

I am also taking running averages of everything, meaning that every week that passes with new completion and start dates, the more data we have on the tracker. The completion date also gets updated automatically. Basically, the more deliverables that are completed based on total known deliverables, would ultimately result in a guarantee of finished project deliverables when the last deliverable is completed. A satisfying feeling indeed. Phew.

With the tracker about finished (ha!) we now have a tentative completion date set for each category (such as Security) for all of our assets. But, if our App Team teams needs security to be completed prior to starting their part, and assuming we are calculating forward (meaning Security hasn't started, but we know how much time they may take) shouldn't there be a way to predict when the dependent team (in this case, App team) should expect the work to arrive based on our calculations? Is this what a data pipeline is? By now I am just becoming familiar with the term scope creep as I try not to blush at the thought of my spreadsheet during the  meeting. 

# The Ingenuity

By this point in the story the word probability becomes more apparent in my mind. Because, that's what statistics is, kind of, right? I should add probability here somewhere. What is the probability that an asset will be completed at one point or another (based on the standard deviations and averages I have set up everywhere). What if Oracle databases are more difficult to work with than SQL Server. Those Oracle assets would likely take longer in the tracker pipeline. Maybe they deserve their own category on the logic table. Could it be that Java apps take more time for permissions to created? Should that be taken into account too?

As I scroll through hundreds of cells and literally-half-a-screen Excel functions my eyes glaze over as I attempt to decipher the best solution for this.  Keep in mind, the Excel tracker I created now looks like a mixture of retired circus memorabilia and the latest overpriced espresso machines on the market. 

I resort again to Google, in hopes of finding the correct statistical regression to be applied. How do I tie everything together? As I skim through the search results the term Poisson comes to mind. By now I'm not sure if I glazed over it, or remembered it from class. Poisson? Poisson equation? How is that spelled? It's French I believe, was it Law of Poiseuille? My engineering background leaning me in that direction.

> Editor's note:  Poisson distribution [Wikipedia](https://en.wikipedia.org/wiki/Poisson_distribution) is part of probability theory, and the Hagen–Poiseuille equation [Wikipedia](https://en.wikipedia.org/wiki/Hagen%E2%80%93Poiseuille_equation), is Fluid Dynamics. 

In my coffee-induced state, I focused on the Physics equation instead of the probability theory as a means of my solution. (I only came to the realization of this mistake very recently, and was my inspiration of this write up). 

![image](https://user-images.githubusercontent.com/9099847/235520883-5ea5fd1c-9d53-4e1f-800b-d267819cc3e2.png)

This could be useful, I thought to myself. I'm working with tracker pipelines, and thinking of workflows. How do I incorporate this to my cute spreadsheet?

![image](https://user-images.githubusercontent.com/9099847/235521067-15d19d3e-7bd4-43d0-a447-a7252ac45d09.png)

Great. This is exactly what I need! Poisson, Poiseuille, it doesn't even matter guy I can get this to work. My spreadsheet has running averages and tentative/expected/confirmed start and completion dates for every asset and work bucket. This means two points for every section (start/end of each bucket) and two points for sending the work between buckets, across (6 or so buckets for the purpose of this writing, but closer to 12), and about 150 rows (assets). That's my ΔP.

>Example: T1 > |Team 1 start date (T1s)> Team 1 end date (T1e)| > T2 | Team 2 start date (T2s) > Team 2 end date (T2e) | > T3

The fluid viscosity (µ) would be similar to the difficulty rating created earlier. A more viscous fluid would take more time between points. 

The length of the pipe (L) is the amount of time for one team to send the work to the subsequent team.

The pipe radius, R, would be our FTE (Full Time Equivalent) - or basically a numeric representation of the amount of man-hours available at any point in time (for each category).

The volumetric flow rate, Q is the amount of time it takes for the fluid to reach the End point from the Start point. (We can also apply this for determining the time it takes inside the bucket such as T1s>T1e as opposed to between buckets bucket-transfer T1 > T2).







#

[Excel functions]


# The Result


# The Outcome

For those that utilize Agile, this story may have sounded more and more familiar. It's humorous to me today (even with the project having been Agile or Kanban inspired already). The original intent still feels to me a little like creating an early Jira/Confluence dashboard (or at least the inspiration behind the movement) - prior to knowing what Agile even was. As I become a yet more experienced analyst and developer, I plan to keep the inexperience and ingenuity and somehow apply it in a more educated and experienced fashion.

Thanks for reading.

-Pedro



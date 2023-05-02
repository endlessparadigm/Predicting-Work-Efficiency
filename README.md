# Predicting Work Efficiency at Work
A fun anecdote related to a work project where I utilized an incorrectly named statistics equation with successful results and multi-dimensional statistical models to predict deliverable completion rates and team-based efficiency of a corporate data management project.

## Abstract
I had a really fun time as a contractor nearly 10 years ago for a major company. There was the opportunity to create an estimation of when a major data infrastructure project was to be completed. I took it upon myself to create a complex Excel spreadsheet, and apply my statistics knowledge in hopes of assisting the project management team.

> Specific details have been changed regarding the assets involved given that it was a privacy related effort after all! 

> I wrote this in a similar mindset that I had at the time, as a refreshing view of how inexperience unfolds, and how ingenuity often demonstrates a little humor.

# The Details

It's 2014. At this point I am a simple intern with 6 months of corporate experience. I loved Excel functions, and with my ambitions looking towards an analytics related career, I took it upon myself to create an Excel spreadsheet for a $6 million dollar corporate project. There were over 200 in-scope applications, 70+ databases (SQL, Oracle, mainframe and more), and more than 25 business teams involved in the effort. The expectation was to upgrade or change the infrastructure as a means of modernizing an applications' data for the entirety of IT. The project was already underway, I had access to the budget details, dev-hours logged, as well as a well-detailed existing spreadsheet of the progress and completion status of each of the assets to be modernized.

# The Challenge

The project is being very well tracked. Each of the 200+ applications have a pipeline or track for the different IT teams (such as Security, App Devs, and DBA's) involved for their part of the work to be completed. This was operating similar to Agile, shortly before it became more popular in today's corporate environment.

For example:

1. Onboarding (Meet with the application team, share details of the project)
2. Analysis (Review of application and application database) 
3. DEV (Upgrade of asset or asset database)
4. Security (Permissions/Protocols defined and applied)
5. Audit and Monitoring (Scheduling and automation) 
6. Signoff and onboarding (Review with business teams on the outcomes of the deliverable)

We have the dates for when an application begins or completes any of the above sections for all of the assets on the list. This was sufficient for the PM team as they can review the data and check in with a specific team regarding the status of the asset for any section listed above. 

# The Opportunity

As a new contractor/intern, I wanted to stand out as a competent analyst and thought we could find a way to predict the date of completion for each of all of these assets. With all of the data being gathered, I could not only predict when an asset was to be completed, but also how busy each of the teams would be at any given time (based on all of the assignments in their list, and the dates in which the planned work would fall in their bucket). 

I could then use that information as a dependency to predict the progress of subsequent applications and ideally formulate an overall project completion date! Not only that, we could even change the order of all of the work to make sure it gets completed even quicker. They'll love me definitely! Given that it was a multi-year project, I would assume it would prove useful. (It was!)

# The Complication
Having not utilized statistics in a corporate environment before (but with adequate math experience), I begin to search on how to apply predictive analytics based on existing data. One finds themselves quickly immersed in a complicated realm of wikipedia and statistics tutorials. Should I really be using these funny equations to predict when the app guy is finished setting up our folder permissions for Database XYZ?

I set off to build a spreadsheet to be used as a supplement to the tracker. I would import the start/completion dates for each of the sections. With my inexperience, I had my little mind set on determining the average completion time required for each of the work sections; such as - what is the average time it takes to onboard a new asset team to our project from the start of it at onset? 

The more I thought about it, the more complicated it became. Onboarding an app could take as little as an hour (based on our Excel dates, 1 day). When scheduling a meeting for another app, it might not be until next week Thursday that we meet (let's say 8 days from now, so 8 days effort). If I take the average, the result might be the same effort (1 hours' time) but a different elapsed time. ***head scratch*** But the actual work would still take 1 hour. How do I relate that paradigm? There is actual work or effort being done or completed, and there is the amount of time that needs to pass for the completion.


# The Inexperience
At this point I am not consciously aware of the complexity of what I am trying to accomplish. I am setting out to determine how much work each of the engineers among many others in the company are completing daily (an important metric in a still-at-waterfall world), in addition to how much time it takes for them to inform us of such work being done. Useful, right? Not only this - I could then track how the individual-not-the-team lags in relation to his or her peers, and also the delay in response to the work effort for any other team they operate with. (Example: If a security team is particularly slow with the DBA's but not with the app dev's, we could investigate this numeric animosity for even more accurate results). I'll be a manager by midnight!

> At this point, I start to be thankful for the senior engineers I worked with at the time and the patience involved on their part. :)

# The Development

After a few weeks of working on my little side project, I now had a few worksheets laid out featuring some neat things:

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

With the tracker about finished (ha!) we now have a tentative completion date set for each category (such as Security) for all of our assets. But, if our App Team teams needs security to be completed prior to starting their part, and assuming we are calculating forward (meaning Security hasn't started, but we know how much time they may take) shouldn't there be a way to predict when the dependent team (in this case, App team) should expect the work to arrive based on our calculations? Is this what a data pipeline is? By now I am just becoming familiar with the term scope creep as I try not to blush at the thought of opening my spreadsheet during a meeting. 

# The Ingenuity

By this point in the story the word probability becomes more apparent in my mind. Because, that's what statistics is, kind of, right? I should add probability here somewhere. What is the probability that an asset will be completed at one point or another (based on the standard deviations and averages I have set up everywhere). What if Oracle databases are more difficult to work with than SQL Server? Those Oracle assets would likely require more time in the tracker pipeline. Maybe they deserve their own category on the logic table. Could it be that Java apps take more time for permissions to be created? Should that be taken into account too?

As I scroll through hundreds of cells and literally-half-a-screen Excel functions my eyes glaze over as I attempt to decipher the best solution for this. Keep in mind, the Excel tracker I created now looks like a mixture of circus memorabilia and the latest overpriced espresso machines on the market. 

I resort again to Google, in hopes of finding the correct statistical regression to be applied. How do I tie everything together? As I skim through the search results the term Poisson comes to mind. By now I'm not sure if I read over it, or remembered it from class. Poisson? Poisson equation? How is that spelled? It's French I believe, was it Law of Poiseuille? My engineering background leaning me in that direction.

> Editor's note:  Poisson distribution [Wikipedia](https://en.wikipedia.org/wiki/Poisson_distribution) is part of probability theory, and the Hagen–Poiseuille equation [Wikipedia](https://en.wikipedia.org/wiki/Hagen%E2%80%93Poiseuille_equation), is Fluid Dynamics. 

In my coffee-induced state, my inspiration pointed to the Physics equation instead of the probability theory as a means of my solution. (I only came to the realization of this name mistake very recently, and was the inspiration of this write up). 

![image](https://user-images.githubusercontent.com/9099847/235520883-5ea5fd1c-9d53-4e1f-800b-d267819cc3e2.png)

This could be useful, I thought to myself. I'm working with tracker pipelines, and thinking of workflows. How do I incorporate this to my cute spreadsheet?

![image](https://user-images.githubusercontent.com/9099847/235521067-15d19d3e-7bd4-43d0-a447-a7252ac45d09.png)

Great. This is exactly what I needed! Poisson, Poiseuille, it doesn't even matter guy I can get this to work. My spreadsheet has running averages and tentative, expected, and confirmed start/completion dates for every asset and work bucket. This means two (start/end) points for every section or bucket and two points for sending the work between buckets (from one team to the next team), across (6 or so buckets for the purpose of this writing, but closer to 12), and about 150 rows (assets). That's my ΔP. (There is also the reminder that not all pipelines are the same, and some buckets are either skipped or concurrent buckets can begin depending on the asset. We can probably fix this with a logic table. Let's set that thought aside for now, this is making me thirsty).

The fluid viscosity (µ) would be similar to the difficulty rating created earlier. A more viscous fluid would take more time between points. 

The length of the pipe (L) is the amount of time for one team to send the work to a subsequent team.

The pipe radius, R, would be akin to our FTE (Full Time Equivalent) - or basically a numeric or factoric(?!) representation of the amount of man-hours available at any point in time within the cylinder or pipeline. We have project hours logged thanks to PPM, this part should be easy.

The volumetric flow rate, Q is the amount of time it takes for the fluid to reach the End point from the Start point. (We can also apply this for determining the time it takes inside the bucket such as T1s > T1e (see below), as opposed to between buckets (or bucket-transfer) T1 > T2). Now I just need to explain this to the leadership team! I think they'll be impressed.

> > | T1 > (Team 1 start date (T1s)> Team 1 end date (T1e)) | > T2 > (Team 2 start date (T2s) > Team 2 end date (T2e)) | > T3 |

We can focus on the time it takes (lag time) for one portion of the work to be completed by a team and the subsequent team picking up the work from the dependent team. Similar to the earlier given example, if something is completed Thursday afternoon, the receiving team may not read their email or see their assignment until Monday or later. We could definitely tighten things up here.

Let's utilize our new fancy equation to estimate the time it takes for the different teams to send and receive their work. We have the project hours logged for our staff, so we can simply accomodate for Frank always completing his assignment on Mondays, and Claire only reading her emails after lunch time (and any other possibility, given our spreadsheet). 

> So to re-iterate on our Hagen-Poiseuille equation (is it lunch time yet?)

> From the front view of the pipelines I have built, we can see the different sections and subsequent dependencies, with the additional grey sections demonstrating the lag time between buckets or sections. Emails are not read immediately, resources go on vacation, and we simply account for the discrepancy given that we have a lot of data from this multi-year project.

![image](https://user-images.githubusercontent.com/9099847/235752558-8b578e04-369a-4210-861d-a980539b71ba.png)

> The discrepancy of rectangle sizes above was to demonstrate the difference in our pipe radius, R. Where we get complicated is when we try to understand that some applications may not need every component or section to be completed on its' own behalf, hence a top view of our pipelines:

![image](https://user-images.githubusercontent.com/9099847/235753161-28d49041-ed16-4c3a-bb08-fa28e7df63eb.png)

The model that we have above actually works great. We have different pipelines, and a little bit of VBA or Excel function manipulation should provide us with this equation working the same anywhere as intended. I also kept my previous calculations to compare the two estimates and to keep one another in check.

# The Exaggeration

This is where my inexperience begins to outshine my wit and willpower. We have to take this one step further, I thought. We have a weighted estimate of when each component is to be completed. We also have an estimate on the delay present for components to be handed off to other teams. We even have the running averages and next-on-queue dependencies set up. The spreadsheet is quite operational. 

What we are missing is the final tie in. The spreadsheet is dynamic in that it waits for the next item in queue based on dates, but calculates the overall effort in its' own unit of measurement (It almost smells like machine learning!). Simply put, the total work remaining is seen as a big tub of mysterious liquid, and the calculator simply compiles this as manpower. The output of this mysterious liquid becomes a known variable, re-feeding the calculator to make it more accurate. 

See below for an example of how we are feeding our calculator with our pipeline.

![image](https://user-images.githubusercontent.com/9099847/235750844-ac3c947a-0601-47dc-83d9-db9526904414.png)

> So this bucket of metaphorical viscous liquid is a resultant of actual people working, and the actual digital (or paper) deliverable being provided. It probably does look like mush when you mix it all up.

We want to utilize the actual values above to help calculate the future values calculated below. We repeat this each time we get more data to ensure a more accurate estimate.

![image](https://user-images.githubusercontent.com/9099847/235751153-98533812-1ca0-4873-88a5-d70e49f9d73f.png)

As I sip on my afternoon soda I try to pinpoint my missing piece. This is automated quite well, how do we make it smart? The spreadsheet needs to be defined in a way that it understands the calculations being executed, and knows how to optimize dependencies on its' own behalf. Could it output suggestions of whether we put our Workday app above our Sharepoint app in priority and have security start it in May as opposed to June? This could in turn create an opening for a different app to begin even earlier, helping to remove an unforeseen roadblock that is already present 3 months from now. Can Excel still handle all of this?!

Let's create an additional calculation layer, I thought to myself. We can map out the running averages for our estimates of each app category based on our logic table to a set of temporary 2-dimensional worksheets, iterate through a series of factors of possible variations, and create a resultant worksheet to mark the fluctuation and degree of success for all of the resulting events. We're basically creating multiple 2-dimensional arrays for the running averages, a matching running set of worksheets set perpendicularly to the 2-D arrays as a way to track these fluctuations, and in the end feeding the resultants to an additional worksheet recording these computations. 

By now my mental treadmill is on the third story of our two floor building. By this point, I simply left the spreadsheet as it was as I began to receive other responsibilities at my job. I believe the final or specific portion that led to me losing interest on it, was having the temporary arrays (mid-operation) select, and tentatively place different order or priority of work in the queue in order to find an earlier target completion date in the calculation. Next time I'll just use Python.

# The Result

I received many good reviews on the tracker. It was a helpful tool to assist the PM's and management for this major undertaking. My ambitious goal of multiple arrays was not in vain. I am happy I had the opportunity to work on my little tracker. Was it accurate? It was accurate enough. With more programming, DevOps, and analytics experience, I realize how large of an undertaking it was, and the thought experiment was excellent. I do believe this to be a yet useful tool that whispers to me for a modern upgrade. Maybe this bad boy will get the respect it deserves by receiving an ML or Deep Learning treatment from me in the future. 

# The Conclusion

For those that utilize Agile, this story may have sounded more and more familiar. It's humorous to me today (even with the project having been Agile or Kanban inspired already). The original intent still feels to me a little like creating an early Jira/Confluence dashboard (or at least the inspiration behind the movement) - prior to knowing what Agile even was. I also learned that Statistics is not quite an intuitive subject as many of us wish for it to be. I was more comfortable wrangling an engineering equation rather than accomodating for the form in which Stats operates on. As I become a yet more experienced analyst and developer, I intend to keep my optimistic ingenuity and continue to apply my learnings in a more elegant fashion.

Thanks for reading.

-Pedro



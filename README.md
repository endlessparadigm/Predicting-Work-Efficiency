# Predicting-Work-Efficiency at Work
Work project utilizing Hagen-Poiseuille equation and 4-dimensional models to predict efficiency-per-team completion rate of a corporate data management project.

## Abstract
I had a really fun time as a contractor nearly 10 years ago for a major company. There was the opportunity to create an estimation of when a major data infrastructure project was to be completed. I took it upon myself to create a complex Excel spreadsheet, and apply my statistics knowledge in hopes of assiting the project management team.

> Specific details have been changed regarding the assets and topics involved given that it was a privacy related effort after all! :)

> I wrote this in a similar mindset that I had at the time, as a refreshing view of how inexperience unfolds, and when ingeniuity shows its' worth.

# The Details

It's 2014. At this point I am a simple intern with 6 months of corporate experience. I loved Excel functions, and with my ambitions looking at an analytics related career, I took it upon myself to create an Excel spreadsheet for a $6 million dollar corporate project. There were over 200 in-scope applications, 70+ databases (SQL, Oracle, mainframe and more), and more than 25 business teams involved in the effort. The expectation was to upgrade or change the infrastructure as a means of modernizing an applications' data for the entirety of IT. The project was already underway, I had access to the budget details, dev-hours logged, as well as a well-detailed existing spreadsheet of the progress or completion status of each of the assets to be modernized.

# The Challenge

The project is being very well tracked. Each of the 200+ applications have a pipeline or track for the different IT teams (Security, App Devs) involved for their part of the work to be completed. This was operating similar to Agile, shortly before it became more popular in today's corporate environment.

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

As a new contractor/intern, I wanted to stand out as a competent analyst and thought we could find a way to predict the date of completion of each of all of these assets. With all of the data being gathered, I could not only predict when an asset was to be completed, but also how busy each of the teams would be at any given time (based on all of the assignments in their list, and the dates in which the planned work would fall in their bucket). I could then use that information as a dependency to predict the progress of subsequent applications and ideally formulate an overall project completion date! Not only that, we could even change the order of all of the work to make sure it gets completed even quicker. They'll love me definitely! Given that it was a multi-year project, I would assume it would prove useful. (It was!)

# The Complication
Having not utilized statistics in a corporate environment before (but with adequate math experience), I begin to search on how to apply predictive analytics based on existing data. One finds themselves quickly immersed in a complicated realm of wikipedia and statistics tutorials. Should I really be using these funny equations to predict when the app guy is finished setting up our folder permissions for Database XYZ?

> Further complexity

>There is additional complexity involved the project. Not all assets utilize all work assignments. Some assets have no work assignments but need to be logged. 

# The Development
I set off to build a spreadsheet to be used as a supplement to the tracker. This would import the start/completion dates for each of the sections. With my inexperience, I had my little mind set on determining the average completion time required for each of the work sections; such as - what is the average time it takes to onboard a new asset team to our project from the start of it at onset? The more I thought about it, the more complicated it became. Onboarding an app could take as little as an hour (based on our Excel dates, 1 day). When scheduling a meeting for another app, it might not be until next week Thursday that we meet (let's say 8 days from now, so 8 days effort). If I take the average, the result might be the same effort (1 hours' time) but a different elapsed time. ***head scratch*** But the actual work would still take 1 hour. How do I relate that paradigm? There is actual work or effort being done or completed, and there is the amount of time that needs to pass for completion.

# The Inexperience
At this point I am not consciously aware of the complexity of what I am now trying to accomplish. I am setting out to determine how much work each of the engineers among many others are completing daily (an important metric in a still-at-waterfall world), in addition to how much time it takes for them to inform us of such work being done. Useful, right? Not only this - I could then track how the individual-not-the-team lags in relation to his or her peers, and also the response rate for any other team they operate with. (Example: If a security team is particularly slow with the DBA's but not with the app dev's, we could investigate this numeric animosity for even more accurate results). I'll be a manager by midnight!

> At this point, I start to be thankful for the senior engineers I worked with at the time and the patience involved on their part. :D

# The Ingenuity
--


# The Outcome

For those that utilize Agile, this story may have sounded more and more familiar. It's humorous to me today (even with the project having been Agile or Kanban inspired already). The original intent still feels to me a little like creating an early Jira/Confluence dashboard (or at least the inspiration behind the movement) - prior to knowing what Agile even was. As I have become a more experienced analyst and developer, I plan to keep the inexperience and ingenuity and somehow apply it in a more professional and experienced fashion.

Thanks for reading.

-Pedro



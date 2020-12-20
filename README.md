# Project 1: SAT & ACT Analysis
## Executive Summary
In the United States, the SAT and ACT are entrance exams used by colleges and universities to make admission decisions. These exams help provide colleges with a common data point that can be used to compare all applicants. While many colleges do not prefer one test over the other, and while both tests share a number of similarities in terms of subjects tested, participation rates for each test tend vary wildly across the country.

In 2016, the College Board implemented major changes to the SAT in an attempt to counter the growing popularity of the ACT. By looking at data from the subsequent years of 2017 and 2018, we can begin to measure the impact of these changes, while coming up with new strategies that may help the College Board increase their participation rates moving forward.

<b>Problem Statement: which state should the College Board target to further raise SAT participation rates?</b>

## Summary and Recommendations
We found that states with a relatively low GDP per Capita and high ACT participation rate tend to get lower ACT scores on average. The opposite is true for states with a relatively low GDP per Captia that take the SAT. This could make a compelling argument for states that are looking to improve their position on the National Assessment of Educational Progress (NAEP).

<img src="/assets/avg_score_scatter.png" width=1000 vertical-align=middle style=max-width:100%;>

Given that North Carolina falls into the above group (high ACT participation, relatively low GDP, below average ACT scores) and has not yet committed to the Innovative Assessment pilot, <b>I recommend that the College Board work with North Carolina to raise SAT participation rates.</b>

However, the College Board must take into account the growing movement against standardized testing. Instead of trying to pile on additional tests, the College Board must partner states in their effort to reduce over-testing and market the SAT as a tool to help with this process.

Beyond just signing a contract with a state, the College Board should also look to incorporate other forms of testing such as portfolio-based assessment or adaptive testing.

With COVID-19 heavily affecting standardized testing throughout the United States and further pushing states to consider the alternative means of assessment, the College Board must continue to adapt the SAT to fit the times that we are now in.


## Additional Research
Participation rates in the SAT and ACT are largely determined by state education policy. The largest jumps in SAT and ACT participation in 2018 were due to states like [Colorado switching from the SAT and ACT](https://www.coloradoindependent.com/2017/07/06/from-csap-to-parcc-heres-how-colorados-standardized-tests-have-changed-and-whats-next/), leading to a massive jump in their SAT participation rate from 11% to 100%. Accordingly, ACT participation rates dropped from 100% to 30%. Illinois also had a similar jump, from 9% in 2017 to 99% in 2018, due to the state [switching to the SAT in 2018](https://chicago.chalkbeat.org/2018/7/27/21105418/illinois-has-embraced-the-sat-and-the-act-is-mad-about-it#:~:text=The%20ACT%20protested%2C%20arguing%20that,the%202016%2D17%20school%20year.).

Hawaii is particularly interesting as the state is unique in terms of its location and demographics. The majority of Hawaiians live in urban areas, which seems to be contrary to the trend of urban/coastal states favoring the SAT test. One of the reasons behind high SAT and ACT participation rates could be due to Hawaii's strong testing culture, which can be traced back to the federal 'No Child Left Behind' law, when Hawaii won a $75 million Race to the Top grant that [established performance outcomes tied to test scores](https://www.civilbeat.org/2018/04/hawaii-teachers-think-your-kids-are-taking-way-too-many-tests/). This suggests that schools are pushing for standardized testing beyond the norm. The ACT participation rate is greater than the SAT participation rate as public schools started made the [ACT mandatory for all Hawaii public school juniors starting from 2014](https://www.hawaiinewsnow.com/story/32835151/hawaii-students-perform-better-on-act-but-scores-still-lag-behind-nation/).

A common trend in states with above 50\% participation for both the SAT and ACT has been the rise of [a counter-movement against standardized testing in general](https://www.edweek.org/ew/articles/2018/10/11/what-happens-when-state-un-standardize-tests.html). States like [Georgia and North Carolina](http://blogs.edweek.org/edweek/campaign-k-12/2018/10/essa-innovation-testing-georgia-kansas-south-carolina-hawaii.html?cmp=soc-edit-tw) signed on to the Innovative Assessment pilot launched by the US government in 2018, which is a programme that intends to use different assessment methods as an alternative to traditional standardized tests. [Hawaii and South Carolina](http://blogs.edweek.org/edweek/campaign-k-12/2018/10/essa-innovation-testing-georgia-kansas-south-carolina-hawaii.html) have also signalled interest in the program.

The high ACT/SAT participation rates in Florida are likely due to the [mandatory Florida Statewide Assessments](http://www.flvs.net/student-resources/full-time/statewide-assessment-testing#:~:text=Florida%20Statewide%20Assessment%20Program,achievement%20of%20the%20Florida%20Standards) (FSA).  This means that students who want to apply to out of state universities still need to take the SAT and ACT. While some school officials have tried to push for the adoption of the SAT or ACT over local assessments and reduce standardized testing in general, the state has argued that the [ACT and SAT is unable to replace the FSA](http://www.fldoe.org/core/fileparse.php/5663/urlt/ACTSATFSA.pdf).  There continues to be [further pushback against standardized testing](https://feaweb.org/news/frontline/overtesting-of-floridas-students/) in Florida.

## Datasets
- [2017 & 2018 SAT Scores](http://ipsr.ku.edu/ksdata/ksah/education/6ed16.pdf) (Kansas University)
- [2017 ACT Scores](https://www.act.org/content/dam/act/unsecured/documents/cccr2017/ACT_2017-Average_Scores_by_State.pdf) (ACT)
- [2018 ACT Scores](https://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf) (ACT)
- [2017 US Party Affiliation by State](https://news.gallup.com/poll/226643/2017-party-affiliation-state.aspx) (Gallup)
- [2018 US Party Affilation by State](https://news.gallup.com/poll/247025/democratic-states-exceed-republican-states-four-2018.aspx) (Gallup)
- [2017 & 2018 GDP per Capita](https://apps.bea.gov/iTable/) (US Bureau of Economic Analysis)

## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|SAT_2017 |State from which ACT and SAT data was collected| 
|**sat_2017_participation**|*integer*|SAT 2017 |Participation rate as a percentage out of 100|
|**sat_2017_reading_and_writing**|*integer*|SAT 2017 |Average score for reading and writing (Min: 200, Max: 800)|
|**sat_2017_math**|*integer*|SAT 2017|Average math score (Min: 200, Max: 800)|
|**sat_2017_total**|*integer*|SAT 2017|Average total score (Min: 400, Max: 1600)|
|**act_2017_participation**|*integer*|ACT 2017 |Participation rate as a percentage out of 100|
|**act_2017_english**|*float*|ACT 2017|Average english score (Min: 1, Max:36)|
|**act_2017_math**|*float*|ACT 2017|Average math score (Min: 1, Max:36)|
|**act_2017_reading**|*float*|ACT 2017|Average reading score (Min: 1, Max:36)|
|**act_2017_science**|*float*|ACT 2017|Average science score (Min: 1, Max:36)|
|**act_2017_total**|*float*|ACT 2017|Average total score derived as a composite of Math, Reading, English and Science scores (Min: 1, Max:36).|
|**sat_2018_participation**|*integer*|SAT 2018 |Participation rate as a percentage out of 100|
|**sat_2018_reading_and_writing**|*integer*|SAT 2018|Average score for reading and writing (Min: 200, Max: 800)|
|**sat_2018_math**|*integer*|SAT 2018|Average math score (Min: 200, Max: 800)|
|**sat_2018_total**|*integer*|SAT 2018|Average total score (Min: 400, Max: 1600)|
|**act_2018_participation**|*integer*|ACT 2018|Participation rate as a percentage out of 100|
|**act_2018_english**|*float*|ACT 2018|Average english score (Min: 1, Max:36)|
|**act_2018_math**|*float*|ACT 2018|Average math score (Min: 1, Max:36)|
|**act_2018_reading**|*float*|ACT 2018|Average reading score (Min: 1, Max:36)|
|**act_2018_science**|*float*|ACT 2018|Average science score (Min: 1, Max:36)|
|**act_2018_total**|*float*|ACT 2018|Average total score derived as a composite of Math, Reading, English and Science scores (Min: 1, Max:36).
|**gdp_2017**|*integer*|US BEA|Real estimates of Gross domestic product (GDP) by state measured in chained 2009 dollars
|**gdp_2018**|*integer*|US BEA|Real estimates of Gross domestic product (GDP) by state measured in chained 2009 dollars
|**cat_gdp_2017**|*object*|US BEA|Real estimates of Gross domestic product (GDP) by state measured in chained 2009 dollars, sorted by category (<40000, 40000-50000, 50000-60000, >60000)
|**cat_gdp_2018**|*object*|US BEA|Real estimates of Gross domestic product (GDP) by state measured in chained 2009 dollars, sorted by category (<40000, 40000-50000, 50000-60000, >60000)
|**classification**|*object*|Gallup|Political affliation by state based on annual state averages of party affiliation (Democrat, Republican and Swing)
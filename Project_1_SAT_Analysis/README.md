# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

##### by: Lin Junyuan, SG-DSI-14

## Introduction
SAT introduced a new format in 2016. Being an employee of the College Board, my role is to track statewide participation rates and score results. Using the data collected, the objective is to recommend where to invest money to improve SAT participation rates.

## Problem Statement

**What is the best state to invest money in to raise SAT participation rates?**

## Executive Summary

This project attempts to identify the best candidate state to invest in to improve participation rates. The data provided initially are two years' worth (2017 and 2018) of participation rates in percentages and mean scores in individual subjects as well as the Total/Composite scores, organized by state.

Initial analysis of the data shows a rather consistent relationship between some of the variables. 
- In every state, there is an inverse relationship between the participation rate of any of the tests and its mean scores, meaning low participation results in high mean test scores, and vice versa,
- Between tests, there is also an inverse relationship in their participation rates. States with high ACT participation tends to have low SAT participation, and vice versa.

However, it is not recommended to directly compare mean scores between ACT and SAT, even in similar subjects. Due to the lack of information such as the state student population and whether there are students who took both tests, statistical inferences cannot be made. 

By using the original data and generating a database that tracks the change in each variable over the course of one year, it is observed that states that has larger change in their participation rates also meet with larger change in their mean scores, and, more interestingly, several states saw rather drastic changes in SAT or ACT participation rates. 

By conducting external research on these states, it is found that state education policy change is the main reason behind the change. By obtaining each state's high school education policy, **South Dakota** is the one of the states with low SAT participation rates and has yet to make either SAT or ACT mandatory for its high school students.

 ## Conclusions and Recommendations

In conclusion, there are inverse relationships 
-   between participation rates of the two tests, 
-   between each test's participation rates and its scores and 
-   also between each test's change in participation rates and its change in scores. 

However, it is more likely that participation rates is the influencing mean scores rather than the other way round. One key takeaway is that states usually prefer one test over another and are likely to focus more on one test only.

Instead, state education policy is the decisive factor that impacts participation rates. From the examples of Colorado and Illinois, the shift of state wide testing from ACT to SAT as mandated by each state's Department of Education proved to be the decisive factor that drastically raised SAT participation rates.

Amongst the states with the lowest SAT participation rates, **South Dakota** does not make either SAT or ACT mandatory for its high school students. It is recommended that the College Board invest money into South Dakota to advocate adopting SAT for their students and educators. 

Taking Illinois as an example , it switched over from ACT to SAT after evaluating SAT's merits despite also being a midwestern state,  where attitudes tend towards using ACT tests score for college admission. The points that Illinois considered were: the revamped format, SAT's supporting programmes such as the reporting system, the  partnership with Khan Academy providing free test preparation and the SAT School day allows lower income families to gain access to colleges. 

 This advocacy can also be extended to South Dakota colleges. As the main driving reason for these tests is for college admission, convincing colleges in this region to be receptive of considering SAT scores will also be helpful.

A potential threat is the test-optional movement. Colleges are increasingly performing admission evaluation without SAT or ACT, claiming that these scores do not necessarily accurately predict student success. Therefore, more studies need to be conducted to verify these claims and strategise how to identify areas which can bring value to colleges that uses SAT scores for admission. This will ensure relevancy and keep SAT participation rates high.



## Data dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|All datasets|The state in USA| 
|sat17_partn|float|SAT 2017|The SAT participation rate (units percent to one decimal place 5.0 means 5.0%)|
|sat17_erw|float|SAT 2017|The state average Evidence Based Reading and Writing score|
|sat17_math|float|SAT 2017|The state average Math score|
|sat17_total|float|SAT 2017|The state average Total score|
|act17_partn|float|ACT 2017|The ACT participation rate (units percent to one decimal place 5.0 means 5.0%)|
|act17_eng|float|ACT 2017|The state average English score|
|act17_math|float|ACT 2017|The state average Math score|
|act17_rdg|float|ACT 2017|The state average Reading score|
|act17_sci|float|ACT 2017|The state average Science score|
|act17_comp|float|ACT 2017|The state average Composite score|
|sat18_partn|float|SAT 2018|The SAT participation rate (units percent to one decimal place 5.0 means 5.0%)|
|sat18_erw|float|SAT 2018|The state average Evidence Based Reading and Writing score|
|sat18_math|float|SAT 2018|The state average Math score|
|sat18_total|float|SAT 2018|The state average Total score|
|act18_partn|float|ACT 2018|The ACT participation rate (units percent to one decimal place 5.0 means 5.0%)|
|act18_eng|float|ACT 2018|The state average English score|
|act18_math|float|ACT 2018|The state average Math score|
|act18_rdg|float|ACT 2018|The state average Reading score|
|act18_sci|float|ACT 2018|The state average Science score|
|act18_comp|float|ACT 2018|The state average Composite score|
|sat_partn_change|float|Year-on-year|Change in SAT participation rates between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)|
|sat_erw_change_pct|float|Year-on-year|Percentage change in SAT Evidence Based Reading and Writing score between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)|
|sat_math_change_pct|float|Year-on-year|Percentage change in SAT Math score between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)|
|sat_total_change_pct|float|Year-on-year|Percentage change in SAT Total score between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)
|act_partn_change|float|Year-on-year|Change in ACT participation rates between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)|
|act_eng_change_pct|float|Year-on-year|Percentage change in ACT English score between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)
|act_math_change_pct|float|Year-on-year|Percentage change in ACT Math score between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)
|act_sci_change_pct|float|Year-on-year|Percentage change in ACT Science score between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)
|act_comp_change_pct|float|Year-on-year|Percentage change in ACT Composite score between 2017 and 2018 (units percent to one decimal place 5.0 means 5.0%)
|sat_reqd|bool|2018|Whether SAT is a mandatory requirement in the state as of 2018. True : Yes, False : No
|act_reqd|bool|2018|Whether ACT is a mandatory requirement in the state as of 2018. True : Yes, False : No

## File Navigation
```
Project_1_SAT_Analysis
|
|-- README.md (This file!)
|-- SAT_rec_slides.pdf (Presentation slides)
|-- code
|   |-- SAT_analysis.ipynb (Jupyter notebook)
|-- data
    |-- act_2017.csv
    |-- act_2018_updated.csv
    |-- combined_2017.csv
    |-- final.csv
    |-- sat_2017.csv
    |-- sat_2018.csv
    |-- state_requirements_2018.csv
```

## Data sources

### Provided

As part of the project, [ACT 2017](./data/sat_2017.csv), [ACT 2018](./data/act_2018_updated.csv), [SAT 2017](./data/sat_2017.csv) and [SAT 2018](./data/sat_2018.csv) files were provided. These sources of these data were pulled from the links below:
- [SAT 2017](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/) 
- [ACT 2017](https://www.act.org/content/dam/act/unsecured/documents/cccr2017/ACT_2017-Average_Scores_by_State.pdf) 
- [SAT 2018](https://reports.collegeboard.org/sat-suite-program-results/state-results) 
- [ACT 2018](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf)

### External
1. Gorski, E. ( December 23, 2015) Goodbye ACT, hello SAT: a significant change for Colorado high schoolers. Retrieved from https://chalkbeat.org/posts/co/2015/12/23/goodbye-act-hello-sat-a-significant-change-for-colorado-high-schoolers/
2. Wheeler, D. (January 8, 2017) Colorado Changed to the SAT in 2017: What You Need to Know. Retrieved from https://www.testive.com/colorado-sat-change-2017/
3. (January 2016) Colorado’s Switch from ACT to SAT Retrieved from https://www.coloradokids.org/wp-content/uploads/2016/01/ACTvsSAT_FINAL.pdf
4. Rado, D. (February 11, 2016) Illinois moves ahead with new testing plan, replacing ACT with SAT. Retrieved from https://www.chicagotribune.com/news/ct-illinois-chooses-sat-met-20160211-story.html
5. Wolf, T. (December 21, 2015) Illinois switching from ACT, will give students SAT instead. Retrieved from https://www.bnd.com/news/local/article50939170.html
6. Gilchrist, S. (February 28, 2017) Ohio schools must now give ACT or SAT to all juniors. Retrieved from https://www.dispatch.com/news/20170228/ohio-schools-must-now-give-act-or-sat-to-all-juniors
7. Safier, R. (March 19, 2016) New SAT Format: What It Means for You. Retrieved from https://blog.prepscholar.com/new-sat-format-2016
8. Anderson , N. (September 24, 2019) SAT scores drop for s2019 class, but participation rises through testing in schools. Retrieved from https://www.washingtonpost.com/local/education/sat-scores-drop-for-2019-class-but-participation-rises-through-testing-in-schools/2019/09/23/332fc4d0-de11-11e9-8dc8-498eabc129a0_story.html
9. March, K. (May 3, 2018) Does your state require the SAT or ACT? Retrieved from https://www.testive.com/state-sat-act/
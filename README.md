# Data Analytics Capstone: Atlas Interactive Case Study
## Introduction
In this case study, I will perform many real-world tasks of a junior data analyst at a fictional company, Atlas Interactive. In order to answer the key business questions, I will follow the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.
### Quick links:
Data Source: [kaggle_dataset](https://www.kaggle.com/datasets/rabieelkharoua/predict-online-gaming-behavior-dataset) [accessed on 11/11/25]

Data Visualizations: [Tableau](https://public.tableau.com/app/profile/jerry.soh/viz/game-playertype-casestudy/AveragePlayTimeHoursByPlayerType)
## Background
### Atlas Interactive
Atlas Interactive is the publisher of Shadow City Saga, an immensely popular Open-World Action-Adventure game. The game boasts a massive player base and generates revenue through microtransactions and Downloadable Contents (DLCs). Atlas Interactive sets itself apart from other publishers by continuously releasing free content updates, new maps for exploration, and inclusive multiplayer modes, making the game appealing to a variety of gamers. The vast majority of players are Casual while a much smaller, highly engaged segment comprises the Hardcore Players.

Until now, Atlas Interactive's marketing strategy relied on raising brand awareness and appeal to the broad consumer segments. One strategy used was the flexibility of its access and purchase model: basic game purchase, premium battle passes (seasonal), and VIP-tier subscription memberships.

Customers who only made basic game purchases and standard in-game purchases are referred to as Casual Players while those who frequently purchase the premium battle passes and/or the recurring VIP-tier subscription membership are considered Hardcore Players.

Atlas Interactive’s financial analysts have concluded that Hardcore Players contribute more to the game’s profits than Casual Players due to their higher lifetime value (LTV) and consistent spending habits. Although the flexible purchase model helps attract more customers, Moreno (the marketing director and my manager) believes that maximising the number of Hardcore Players will be key to future profit growth and stability. Rather than creating a marketing campaign that targets all customers, Moreno believes that converting high-potential Casual Players into Hardcore Players is more desirable. This is because she observes that Casual Players are already invested in the Shadow City Saga world and have chosen the game for their entertainment needs.

Moreno has set a clear goal: Design marketing and product strategies aimed at converting Casual Players into Hardcore Players. However, the marketing analyst team needs to better understand how Hardcore and Casual Players differ, what motivates the former to invest more, and how digital channels (like in-game promotions, email, and social media) could affect their marketing tactics. Moreno and her team are interested in analyzing the Shadow City Saga historical player behavior data to identify conversion trends.

## Scenario 
I assume the role of Junior Data Analyst working in the marketing analyst team at Atlas Interactive. The marketing director believes the company’s future success depends on maximising Hardcore Players count. Therefore, my team needs to understand how Casual Players and Hardcore Players engage with Shadow City Saga respectively. These insights would enable my team to design a new marketing strategy aimed at converting Casual Players into Hardcore Players. However, Atlas Interactive executives must approve our recommendations, hence the strategy must be backed up with compelling data insights and professional data visualisations.

## Ask
### Business Task
Devise marketing and product strategies to convert Casual Players into Hardcore Players to maximise the lifetime value of Shadow City Saga.
### Analysis Questions
Three questions will guide the future conversion programme:
1. How do Hardcore Players and Casual Players play Shadow City Saga differently?
2. What behavioral or in-game reward factors would motivate a Casual Player to transition into a Hardcore Player?
3. How can Atlas Interactive use marketing channels and in-game promotions to convince Casual Players to become Hardcore Players?

## Prepare
### Data Source
I will use Atlas Interactive’s historical gaming data to analyse and identify trends which can be downloaded from [kaggle_dataset](https://www.kaggle.com/datasets/rabieelkharoua/predict-online-gaming-behavior-dataset). The data has been made available by [Creative Commons](https://creativecommons.org/licenses/by/4.0/) under this license.

This is public data that can be used to explore how different types of players play Shadow City Saga. But note that data-privacy issues prohibit from using players’ personally identifiable information. This means that we won’t be able to connect in-game purchases to credit card numbers to determine if casual players have purchased multiple premium battle passes and/or the recurring VIP-tier subscription membership.

### Data Organization
There is one spreadsheet that contains data such as player id, demographics, game type, engagement time, quantity of purchase, gameplay level and progression. The corresponding column names are: PlayerID, Age, Gender, Location, GameGenre, PlayTimeHours, InGamePurchases, GameDifficulty, SessionsPerWeek, AvgSessionDurationMinutes, PlayerLevel, AchievementsUnlocked, EngagementLevel. 

## Process
Spreadsheet is used to work on the dataset and clean it.
Reason:
A spreadsheet can handle up to 10,000,000 cells in Google Sheets. Since Atlas Interactive’s dataset has 520,429 cells (40,033 rows x 13 columns), a spreadsheet is sufficient in handling this volume of data.
### Data Exploration & Cleaning
Before cleaning the data, I familarise myself with the data to understand its meaning. Thereafter, I will remove and modify irrelevant data to suit this project’s needs.  

Observations and actions:
1. The table below shows all column headers: 

PlayerID
Age
Gender
Location
GameGenre
PlayTime
Hours
InGame
Purchases
GameDifficulty
SessionsPerWeek
AvgSession
DurationMinutes
PlayerLevel
Achievements
Unlocked
Engagement
Level

2. Data preparation streamlined the dataset by removing non-essential fields. Since the core business objective is to identify factors influencing the conversion of Casual to Hardcore Players, the demographics data [ie. Age (Column B), Gender (Column C), and Location data (Columns D)] are excluded from the final dataset. This allows the concentration of  analytical effort exclusively on the behavioral metrics that directly measure player engagement and commitment.

  ![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image12.png) 

3. Data filtering was performed to maximise analytical precision relative to the project scope. Since the project focuses only on Shadow City Saga, an Open-World Action-Adventure game, the dataset was filtered to exclude all rows of data where GameGenre (Column B)  does not contain the word “Action” (ie. RPG, Simulation, Sports, Strategy). This refined the focus to player behavior specifically within the relevant "Action" category.

 ![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image13.png)
 ![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image8.png)

### Summary
1. All irrelevant columns of demographic data (ie. Age, Gender, and Location data) are deleted.
2. Rows of data where the GameGenre Column does not indicate that the game played by the users is “Action” are excluded.
3. A total of 31,993 rows and 3 columns of irrelevant data are removed in this step

## Analyze and Share
Data Visualization: [Tableau](https://public.tableau.com/app/profile/jerry.soh/viz/game-playertype-casestudy/AveragePlayTimeHoursByPlayerType) 

The data is cleaned and stored appropriately and is now prepared for analysis. I visualised the analysed results in Tableau.
The first analysis question is: How do Hardcore Players and Casual Players play Shadow City Saga differently? (Diagnosis)
This question focuses on descriptive analysis and comparison of key behavioral metrics across the defined segments (Casual vs Hardcore) and the intermediate segments of Low, Medium, and High Engagement.

### 1. Analysis of TotalPlayTimeHours (Total Time Investment since starting the game)
The goal of this visualisation is to compare the distribution of cumulative playtime hours for the Low, Medium, and High player segments. I used a Side-by-Side Box Plot (Three Segments) to confirm the lack of distinction in total cumulative hours invested since the players downloaded the game across the engagement levels, proving that total hours is limited in usefulness as a metric for conversion.

### 2. Analysis of SessionsPerWeek (Habit and Frequency)
The goal of this visualisation is to identify the conversion threshold for gaming habit-building by comparing the frequency of sessions logged-in per week across the Low, Medium, and High engagement segments. I used a Side-by-Side Box Plot (Three Segments) because it clearly quantifies the Medium → High conversion gap in frequency, allowing us to isolate the precise gaming habit increase required to move a player into the Hardcore segment.

### 3. Analysis of AvgSessionDurationMinutes (Immersion and Intensity)
The goal of this visualisation is to define the required level of immersion and intensity by comparing the average duration of each gaming session (minutes) across the Low, Medium, and High engagement segments. I used a Side-by-Side Box Plot (Three Segments) because it clearly maps the progressive increase in session commitment, identifying the crucial time threshold necessary for players to fully engage with and value recurring premium content.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image7.png)

### 1. Average Play Time Hours (PlayTimeHours)
#### A. Interpretation
The median average playtime hours is consistent across all three segments: Low (12.46 hrs), Medium (12.17hrs), and High (12.16 hrs). The distributions (quartiles and ranges) are nearly identical, confirming that overall time investment is standardised across the player base.
#### B. Key Insight
Total time investment is not a useful predictor of engagement level or profitability. The fact that the most profitable segment (ie. Hardcore/ High Engagement Players) logged similar total hours to the least engaged (ie. Casual/ Low Engagement Players) proves that conversion is driven by gaming habit (frequency) and intensity (duration), not raw time volume.
#### C. Implications for Strategy
Action: The marketing and product teams should eliminate any strategy that rewards or promotes increasing aggregate playtime. Resources must be focused entirely on influencing the frequency and duration of individual sessions to achieve high conversion rates.

### 2. Sessions Per Week (SessionsPerWeek)
#### A. Interpretation
Session frequency shows a clear, progressive, and defining data: Low Engagement players median average 3 sessions/week, Medium median average 9 sessions/week, and High Engagement median average 15 sessions/week. The hardest behavioral shift is the Low → Medium jump (a ×3 increment), while the Medium → High jump is a smaller, more manageable increase of 6 sessions.
#### B. Key Insight
Gaming habit is the primary, most actionable driver of conversion. The Medium segment (the high-potential target) has already overcome the massive hurdle of infrequent play. The 9→15 sessions/week difference is the key conversion gap that must be closed to maximise Hardcore Player count.
#### C. Implications for Strategy
Action: Design short, daily challenges and incentives specifically for the Medium Engagement segment (median of 9 sessions) to push them past 12 sessions per week (the High-Engagement’s lower quartile). This targeted effort on the smaller, more achievable gap enables efficient use of financial resources.

### 3. Average Session Duration Minutes (AvgSessionDurationMinutes)
#### A. Interpretation
Session intensity also progresses significantly: Low Engagement median duration is 55 minutes, Medium is 84 minutes, and High is 138 minutes. The necessary jump from Medium to High requires a substantial increase of 54 minutes per session, in comparison to the jump from Low to Medium’s 29 minutes, signifying a major increase in commitment.
#### B. Key Insight
Deeper immersion is the requirement for players’ financial commitment. The High Engagement player commits to sessions long enough to fully utilise premium, recurring game features (eg. 138 minutes is enough time to complete a full battle pass track). The Medium segment, while showing commitment (84 minutes), needs a major push in immersion of the game’s content to convert.
#### C. Implications for Strategy
Action: Implement a two-tiered in-game promotion system. Target the Medium Engagement median (84 minutes) with a high-value pop-up or challenge that explicitly requires the VIP subscription or Premium Battle Pass to unlock a major bonus, strategically extending their play into the 138-minute High-Engagement zone.


### 4. Defining Purchase Behavior Across Engagement Segments
The goal of this visualisation is to test the company's hypothesis that Hardcore Players are primarily differentiated by making any in-game purchase, through comparison of the proportion of players who have purchased across the Low, Medium, and High engagement segments. I used a 100% Stacked Bar Chart (Three Segments) because this visual allows for a direct comparison of the purchaser vs. non-purchaser ratio within each segment, providing clear evidence on whether a single initial purchase is a predictor of high engagement.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image2.png)

#### A. Interpretation 
A comparison of the in-game purchase rates reveals no significant difference across the engagement segments. The rate of players who have made at least one purchase is nearly identical: 19.52% for Low, 19.02% for Medium, and 19.67% for High Engagement players. This means over 80% of all players, regardless of engagement level, have never made a purchase.
#### B. Key Insight 
The act of making a single, general in-game purchase is not a distinguishing factor for highly profitable (Hardcore) players. Their higher Lifetime Value (LTV) must be driven by recurring premium spending (eg. VIP subscriptions, Battle Passes) or significantly higher value in subsequent purchases, all concentrated within that small ≈19% purchasing segment.
#### C. Implications for Strategy 
Action: Atlas Interactive should abandon any broad marketing strategies aimed at converting the ≈80% of non-purchasing Casual/ Low and Medium Engagement Players. Instead, the focus must be on an extremely targeted "upsell" strategy on the Medium Engagement players (≈19% of that group) who have already made a purchase.

### 5. Progression Efficiency and Feature Utilisation Analysis
The goal of this visualisation is to define the progression and feature utilisation efficiency by comparing the relationship between Player Level and quantity of Achievements Unlocked respectively across the Low, Medium, and High engagement segments. I used a Scatter Plot with Segmented Trend Lines because this visual effectively shows whether High Engagement players achieve a steeper progression curve (more achievements per level) than the other segments, thus demonstrating greater commitment to the in-game features.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image1.png)

#### A. Interpretation 
The trend lines show an extremely weak correlation between Player Level and Achievements Unlocked for all three segments (Low: R2≈0.0025, Medium: R2≈0.0009, High: R2≈0.0024). The data is highly scattered, with no discernible relationship. Furthermore, the Low Engagement group shows a technically nonsensical, slightly negative slope (∇= −0.0340), confirming the model is invalid for all segments.
#### B. Key Insight 
Progression efficiency (Achievements unlocked per Level) is not a distinguishing behavioral factor for conversion. The lack of any meaningful correlation suggests that the in-game achievement system is either too broad, easy, or ignored by players, rendering it ineffective as a metric for analysis of feature utilisation or deeper engagement.
#### C. Implications for Strategy 
Action: The product team should immediately re-evaluate the design and rewards tied to achievements. Since achievements fail to correlate with engagement, they are not driving deeper feature utilisation. Hence, marketing strategies must rely on the proven differentiators: the significant gaps in Session Frequency and Session Duration found in the previous analyses.

The next analysis question is: What behavioral or in-game reward factors would motivate a Casual Player to transition into a Hardcore Player? (Incentives)
This involves identifying the leading indicators of conversion, focusing on the players in the Medium Engagement group as the prime conversion target.

### 6. Difficulty Preference as an In-Game Motivational Factor
The goal of this visualisation is to identify a clear in-game motivational factor by comparing the distribution of preferred Gameplay Difficulty chosen by players across the Low, Medium, and High engagement segments. I used a 100% Stacked Bar Chart (Three Segments) because it clearly reveals if High Engagement players disproportionately favor a specific difficulty setting. This allows Atlas Interactive to structure conversion rewards (such as exclusive items) around encouraging Medium players to attempt that motivational difficulty level.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image10.png)

#### A. Interpretation 
Easy difficulty is the overwhelmingly dominant preference across all engagement levels (≈50%). However, the proportion of players choosing Hard difficulty peaks within the High Engagement group (21.03%). Notably, the strategic target Medium Engagement group shows the lowest proportional preference for Hard difficulty (18.74%).
#### B. Key Insight 
Tolerance for Hard difficulty is a behavioral indicator of a Hardcore mindset. The slight increase in Hard mode preference for High Engagement players suggests they are motivated by challenges or the unique rewards tied to it. The strategic hurdle is that the Medium Engagement conversion pool is the least motivated by this factor, indicating a reluctance to fully immerse in challenging content.
#### C. Implications for Strategy 
Action: Design in-game promotions and time-limited events specifically to reward Medium Engagement players for attempting and completing Hard mode content. This needs to include high-value, exclusive rewards (eg. premium content unlocks) that are tied only to challenging tasks, thereby associating high difficulty gameplay with Hardcore yet premium experience.

### 7. Progression Gap Target: Median Player Level
The goal of this visualisation is to establish a concrete, actionable progression threshold by comparing the Median Player Level across the Low, Medium, and High engagement segments. I used a Grouped Bar Chart Comparing Medians with a Reference Line because this format clearly isolates the level gap between the Medium Engagement segment and the Hardcore Median Target, allowing the product team to define a specific level goal for conversion rewards.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image6.png)

#### A. Interpretation 
The Median Player Level shows a clear progression: Low (44), Medium (51), and High (52). The majority of the progression effort occurs in earlier stages (a 7-level jump from Low to Medium). The critical conversion gap between the Medium and Hardcore segment is extremely small, requiring only a 1-level increase (Level 51 to Level 52).
#### B. Key Insight 
Player Level is the last behavioral bottleneck for conversion. The Medium player is already at the level required to be Hardcore. This means that transiting from Level 51 to 52 is the critical gateway where players either commit to the necessary high-frequency and long-duration gaming habits (identified in Visualisation #2 and #3) or stagnate.
#### C. Implications for Strategy 
Action: The product team must set the conversion goal at Level 52 and trigger the highest-value, recurring revenue promotions (eg. VIP Pass, Premium Subscription) immediately after players reach Level 51. This creates a hyper-targeted, last-chance incentive to commit financially and behaviorally before the player hits the post-level-51 stagnation point.

### 8. Achievement Gap Target: Reward-Based Motivation
The goal of this visualisation is to establish a clear in-game reward threshold by comparing the Median Achievements Unlocked across the Low, Medium, and High engagement segments. I used a Grouped Bar Chart Comparing Medians with a Reference Line because this format precisely quantifies the achievement gap between the Medium segment and the Hardcore Median Target, which allows the product team to define a concrete reward goal for motivational campaigns.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image4.png)

#### A. Interpretation 
The Median Achievements Unlocked is inconsistent with the engagement progression. Although the Low segment median is 22, the Medium Engagement segment records the highest median achievement count (26), unexpectedly outperforming the Hardcore segment (25). 
#### B. Key Insight 
Achievements do not act as a successful motivational or retention factor. Since Medium players are already out-achieving Hardcore players, there is no achievement gap to close. This strongly confirms the conclusion from the Progression Scatter Plot analysis (Visualisation #5) that unlocking achievements do not reliably drive the long-term gaming habit or financial value associated with the Hardcore segment.
#### C. Implications for Strategy 
Action: Immediately remove the achievement count from any proposed conversion strategy, rewards campaign, or feature-use promotion. The product team needs to investigate if achievements are too easy to obtain and fail to drive sustained player retention. All motivational efforts must be focused on the proven drivers: Session Frequency (Visualisation #2) and Session Duration (Visualisation #3).

### 9. High-Potential Target Pool Synthesis: The Conversion Quadrant
The goal of this synthesis visualisation is to precisely identify the High-Potential Target Pool by mapping the Medium Engagement segment against the two most crucial behavioral thresholds: Session Frequency and Session Duration. We used a Scatter Plot with Two Median Reference Lines because the resulting intersection defines the Hardcore Conversion Quadrant (top-right corner of visualisation), visually isolating the Medium Engagement players who are already adopting Hardcore gaming habits and are therefore the most efficient target for conversion campaigns.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image9.png)
![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image3.png)

#### A. Interpretation 
The High-Potential Target Pool (Medium Engagement players who meet both Hardcore median thresholds) is extremely small, comprising only 0.51% of the entire Medium Engagement segment. In comparison, 21.37% of the High Engagement segment meet this threshold. Interestingly, the Low Engagement segment shows a slightly higher rate of meeting the threshold (0.87%) than the Medium Engagement Segment.
#### B. Key Insight 
Financial efficiency can be maximised due to the size of the target (20). Since less than one percent of the Medium segment is already behaving like a Hardcore player, broad conversion campaigns are inefficient and financially wasteful. The conversion strategy must be laser-focused on that 0.51% cohort, using digital channels to reach them directly and immediately monetise their established high-value behavior.
#### C. Implications for Strategy 
Action: Immediately use behavioral segmentation tools (such as SQL queries on the player database or analytics platform filters) to flag the 0.51% of Medium players who fall into the Conversion Quadrant. The marketing team should execute a high-priority digital campaign (eg. Email, Social retargeting) offering a personalised, high-value incentive (eg. 50% off the first month of VIP Subscription) to convert them instantly, as they represent the target with the highest ​​Return on Investment (ROI) in the entire player base.

The final analysis question is: How can Atlas Interactive use marketing channels and in-game promotions to convince Casual Players to become Hardcore Players? (Strategy)

This involves synthesising the actionable insights from the previous analysis questions to create channel-specific, high-ROI marketing and product recommendations targeting the High-Potential subset of the Medium Engagement group.

Based on the comprehensive behavioral analysis conducted in previous analysis questions, the primary strategic focus for conversion is exclusively the Medium Engagement player segment. This decision is driven by maximised Return on Investment (ROI) and conversion feasibility:
1. Feasibility and Proximity to Target: The Median Medium player is significantly closer to the Hardcore behavioral thresholds (eg. Player Level 51 vs. the Hardcore Level 52, and much higher Session Frequency and Duration than Low players). They have already demonstrated the baseline commitment necessary to form lasting gaming habits.

2. Optimised ROI: Marketing strategy should not target the Low Engagement segment because it exhibits the highest churn risk and requires the greatest promotional effort to change behavior, therefore yielding a low ROI. By focusing on the Medium segment, Atlas Interactive targets the cohort most likely to convert with the smallest promotional nudge.

3. Efficiency of Effort: Concentrating marketing and product resources solely on the Medium segment ensures that campaigns are not diluted across a disengaged population, leading to a higher conversion rate per dollar spent.

### 10. Digital Channel Strategy: Financial Conversion Target
The goal of this visualisation is to define the digital marketing target with the highest Return on Investment (ROI) by comparing the median Sessions Per Week of Medium Purchasers against Non-Purchasers, using the Hardcore Player threshold (median of 15 sessions) as the benchmark. I used a Grouped Bar Chart Comparing Medians with a Reference Line to conclusively test the assumption that past purchase history is a reliable predictor of the frequency needed for Hardcore conversion.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image11.png)

#### A. Interpretation 
The median Sessions Per Week is identical for both Purchasers and Non-Purchasers in the Medium Engagement segment, at 9 sessions per week. Both groups sit significantly below the Hardcore Frequency Target of 15 sessions per week, highlighting a substantial 6-session weekly gap to conversion.
#### B. Key Insight 
Purchaser status is not a predictor of future high engagement. Since Medium Engagement players who have already purchased in-game items share the exact same low gaming habit level (9 sessions/week) as those who have not purchased, digital marketing strategies based on a player's past purchase history are inefficient and should be avoided for the Medium Engagement segment.
#### C. Implications for Strategy 
Action: Digital marketing efforts aimed at player conversion must abandon segmentation by purchase history for the Medium Engagement segment. Instead, Atlas Interactive should use digital channels (such as email, push notifications) to deliver frequency-driven rewards (eg. "Hit 12 Sessions this week, get a bonus item") to all Medium Engagement players, focusing purely on increasing the frequency baseline from 9 towards the Hardcore target of 15.

### 11. Optimal In-Game Prompt Time: Product Specification
The goal of this visualisation is to translate the Hardcore behavioral intensity finding into a precise product specification by analysing the session duration distribution of the Medium Engagement segment. I used a Box Plot with Dual Median Reference Lines because this format clearly shows the current statistical variance and establishes the Hardcore Conversion Prompt Time (138 minutes), which is the exact minute mark the product team should utilise to trigger the highest-value, conversion-focused in-game promotion.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image14.png)

#### A. Interpretation 
The current median average session duration for the Medium Engagement segment is 84 minutes. The vast majority of the segment (75%) concludes their session by the Upper Quartile (123 minutes). The Hardcore Conversion Prompt Time is 138 minutes, which sits beyond the Upper Quartile, highlighting a large 15-minute intensity gap (138−123) that players must cross to reach the Hardcore behavior threshold.
#### B. Key Insight 
The critical decision point occurs between the 123 and 138-minute marks. Since the Hardcore target (138 min) is above the Upper Quartile (123 min), a high-value promotion must be triggered at a time that incentivises the top 25% of Medium players to sustain their session past their natural churn time.
#### C. Implications for Strategy 
Action: The product team must programme the highest-value, recurring purchase promotion (eg. VIP Pass) to trigger precisely at the 138-minute mark. Additionally, a light, preparatory incentive can be delivered at the 123-minute mark (Upper Quartile) to stabilise the session and encourage the player to push beyond their natural duration ceiling toward the 138-minute conversion goal.

### 12. Targeted Difficulty Incentive: Quantifying Challenge-Ready Players 
The goal of this visualisation is to find out the size of the target pool where challenge-based in-game promotions will be presented to them by comparing the number of Medium and High Engagement players who already prefer the Hardest Difficulty setting. I used a Grouped Bar Chart Showing Raw Counts and Percentages because this format clearly establishes the volume of Medium players who are already pre-disposed to the Hardcore behavior of seeking challenge, allowing the product team to efficiently target event rewards toward them.

![image](https://github.com/Jerry5612/data-analyst-portfolio/blob/Jerry5612-images-1/image5.png)

#### A. Interpretation 
The Medium Engagement segment contributes the majority of the combined population currently engaging with the Hardest Difficulty gameplay setting. Specifically, 734 players who choose Hard difficulty are Medium Engagement (62.84% of the combined total), while 434 are High Engagement players (37.16%).
#### B. Key Insight 
Challenge-based rewards have high relevance and volume. The largest pool of players already exhibiting the Hardcore trait of seeking challenge belongs to the target Medium Engagement segment. This pool of 734 players represents a substantial, pre-qualified segment that is highly receptive to promotional events tied to difficulty completion.
#### C. Implications for Strategy 
Action: Immediately launch in-game, time-limited events tied exclusively to the successful completion of Hard difficulty content. The rewards must be highly desirable and exclusive (eg. cosmetic upgrades, unique position titles) to fully capture the 734 challenge-ready Medium Engagement players and push them toward the Hardcore retention mindset.

### Summary
#### Core Habits and Intensity

The analysis of Core Habit (Frequency) shows a significant difference between player groups: Medium Engagement (Casual) players average 9 sessions per week, while Hardcore Engagement (Benchmark) players average 15 sessions per week. The strategy is to target Medium players with frequency-based rewards to push their sessions towards the 15-per-week benchmark. Regarding Core Habit (Intensity), Casual players average 84 minutes per session (though Q3 saw a higher 123 minutes), compared to the Hardcore median of 138 minutes per session. The highest-value promotion should be programmed to trigger precisely at the 138-minute mark, aligning with the product specification.

#### Conversion and Targeting

A critical drop-off point, the Conversion Gateway, was identified at Level 51, where players stagnate and are at high risk of quitting. The benchmark is to sustain progress past Level 52, the defined conversion gateway. Therefore, the strategic action is to reinforce the Level 51 to 52 transition using digital channels.

The Financial Predictor analysis revealed that Purchase Status is identical to Non-Purchasers (both with a median of 9 sessions/week), meaning high frequency and duration are the true differentiators, not the purchase status itself. As a result, the strategy is to abandon Purchase Status as a targeting metric and focus purely on behavioral thresholds.

#### Efficiency and Preferences

For Target Pool Efficiency, the high-potential target pool is extremely small, representing only 0.51% (20 players) of the segment, which is the key efficiency goal. The plan is to hyper-target this 0.51% pool with immediate financial offers to maximize ROI. A strong Challenge Preference was also noted, with a significant pool of 734 players already seeking Hard Difficulty content, a key behavioral trait. Exclusive, difficulty-based events should be launched to capture and retain this 734-player cohort. Finally, the analysis showed that player behavior is not driven by the number of Achievements or Total Lifetime Hours, as differentiation is minimal. These Inefficient Metrics should be excluded from all conversion modeling and marketing efforts.

## Act

### I. Digital Channel Targeting

The first recommendation focuses on Digital Channel Targeting for efficiency. The actionable specification is to immediately flag the 0.51% High-Potential Medium players and deliver high-value, exclusive offers (such as a 50% VIP Pass discount) to convert their established hardcore behavior into immediate revenue. This action is estimated to have a high impact by focusing resources only on the highest ROI targets, thereby minimizing marketing expenditure on low-potential players.

### II. In-Game Product Prompt

The second recommendation involves an In-Game Product Prompt designed to capture revenue at the peak moment of player commitment. This is specified by programming the highest-value promotional trigger, such as a recurring subscription offer, to appear precisely at the 138-minute session mark, which is strategically placed just before the natural player churn point. This approach effectively leverages the behavioral intensity threshold observed in the data.

### III. Retention & Motivation

The final strategy addresses Retention & Motivation. The plan is to launch exclusive, challenge-based events tied to Hard Difficulty completion, targeting the 734 Medium players who have already demonstrated an aspiration for difficult content. The estimated impact is that this action rewards existing aspirational behavior, which successfully reinforces the Hardcore mindset and drives long-term player retention via appealing exclusive content.

## Conclusion

This capstone analysis successfully addressed the core business challenge of converting Casual Players into Hardcore Players by moving beyond general engagement metrics to define precise, actionable behavioral thresholds.

The project established that the Hardcore player mindset is exclusively driven by Session Frequency (15 sessions/week) and Session Duration (138 minutes/session). All other factors, including Purchase History and Achievement Count, were found to be inefficient drivers of long-term retention.

The analysis culminated in the identification of a hyper-efficient High-Potential Target Pool comprising only 0.51% of the Medium Engagement segment and a substantial 734-player cohort ready for challenge. This finding mandates a strategic shift from broad promotional campaigns to a surgical, high-ROI approach.

The resulting three strategic recommendations—including programming the highest-value promotion to trigger precisely at the 138-minute session mark, hyper-targeting the Level 51 → 52 transition, and implementing exclusive challenge-based events tied to Hard Difficulty—provide Atlas Interactive with clear, measurable product specifications. By adopting this data-driven strategy, Atlas Interactive can immediately focus resources on the most motivated players, ensuring that the conversion of this high-potential pool yields a maximum return on investment and significantly boosts the long-term Lifetime Value of Shadow City Saga.

## Executive Summary 

### Business Objective

The main purpose of this analysis is to come up with precise marketing and product strategies to convert Casual Players (Medium Engagement) into Hardcore Players (High Engagement), thereby driving growth in Customer Lifetime Value (LTV) and financial stability for the Shadow City Saga franchise.

### Key Findings & Problem Statement

Analysis of player behavior confirms that the path to profitability is very specific and efficient:
1. The Behavioural Gap: Hardcore behaviour is defined exclusively by Session Frequency (median 15 sessions/week) and Session Duration (median 138 minutes/session). All other metrics (eg. purchase history) lack utility as predictors.

2. The Dual Opportunity: The target pool requires a dual strategy:

  2A. Financial Target: Only 20 Players (0.51%) of the Medium segment are immediately ready for financial conversion offers (as they met both thresholds).

  2B. Retention Target: A large cohort of 734 players is already seeking Hard difficulty content, making them ready for challenge-based retention programs.
  
3. The Conversion Gateway: The highest-risk progression point is the Level 51 → 52 transition, which must be reinforced to prevent player stagnation.

### Strategic Recommendation: Dual-Focus Behavioral Campaign
To maximise ROI and minimise wastage of marketing expenses, the strategy avoids mass-market tactics and employs two distinct, targeted streams based on the player's primary motivation for the game: financial value vs. challenge.

#### High-Potential Financial Pool

The High-Potential Financial Pool consists of a highly valuable, focused group of only 20 players (representing the 0.51% pool). These players are identified by a dual conversion threshold: maintaining 15 or more sessions per week and an average session duration of 138 minutes or more. Driven by a desire to maximize their investment, the promotional focus for this segment will be Recurring VIP Subscription Offers with a direct financial focus.

#### Challenge-Ready Retention Pool

The second segment is the Challenge-Ready Retention Pool, which is a larger group of 734 players. This cohort is distinguished by a clear behavioral conversion signal: a preference for the Hardest Difficulty Mode. Their primary motivation is rooted in seeking challenge and achievement, and the appropriate promotional focus for them is Exclusive, Difficulty-Based In-Game Events with a content focus.

### Implementation & Action

1. Financial Stream Action: Deploy behavioural segmentation tools (eg. specific SQL queries on the player database or analytics platform filters) to flag the 0.51% pool and send hyper-targeted VIP offers to those players.

2. Product Action: Programme the highest-value recurring subscription promotion to trigger precisely at the 138-minute session mark, before natural player churn.

3. Retention Stream Action: Immediately launch exclusive, time-limited content events tied to Hard difficulty completion to capture and reinforce the hardcore gaming habits of the 734 challenge-seeking players.

### Summary Conclusion & Projected Impact

By strictly adhering to this targeted, signal-based approach, the marketing and product budget can be focused entirely on two groups with defined motivations. This methodology guarantees that every dollar and product feature is directed towards a unique, high-potential segment. The strategy converts established hardcore gaming habits into revenue (financial pool) and reinforces aspirational behavior with exclusive content (challenge pool), resulting in a quantifiable and exponential increase in Hardcore Player LTV and count.

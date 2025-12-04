Data Analytics Capstone: Atlas Interactive Case Study
Introduction
In this case study, I will perform many real-world tasks of a junior data analyst at a fictional company, Atlas Interactive. In order to answer the key business questions, I will follow the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.
Quick links:
Data Source: kaggle_dataset [accessed on 11/11/25]
Data Visualizations: Tableau
Background
Atlas Interactive
Atlas Interactive is the publisher of Shadow City Saga, an immensely popular Open-World Action-Adventure game. The game boasts a massive player base and generates revenue through microtransactions and Downloadable Contents (DLCs). Atlas Interactive sets itself apart from other publishers by continuously releasing free content updates, new maps for exploration, and inclusive multiplayer modes, making the game appealing to a variety of gamers. The vast majority of players are Casual while a much smaller, highly engaged segment comprises the Hardcore Players.
Until now, Atlas Interactive's marketing strategy relied on raising brand awareness and appeal to the broad consumer segments. One strategy used was the flexibility of its access and purchase model: basic game purchase, premium battle passes (seasonal), and VIP-tier subscription memberships.
Customers who only made basic game purchases and standard in-game purchases are referred to as Casual Players while those who frequently purchase the premium battle passes and/or the recurring VIP-tier subscription membership are considered Hardcore Players.

Atlas Interactive’s financial analysts have concluded that Hardcore Players contribute more to the game’s profits than Casual Players due to their higher lifetime value (LTV) and consistent spending habits. Although the flexible purchase model helps attract more customers, Moreno (the marketing director and my manager) believes that maximising the number of Hardcore Players will be key to future profit growth and stability. Rather than creating a marketing campaign that targets all customers, Moreno believes that converting high-potential Casual Players into Hardcore Players is more desirable. This is because she observes that Casual Players are already invested in the Shadow City Saga world and have chosen the game for their entertainment needs.
Moreno has set a clear goal: Design marketing and product strategies aimed at converting Casual Players into Hardcore Players. However, the marketing analyst team needs to better understand how Hardcore and Casual Players differ, what motivates the former to invest more, and how digital channels (like in-game promotions, email, and social media) could affect their marketing tactics. Moreno and her team are interested in analyzing the Shadow City Saga historical player behavior data to identify conversion trends.
Scenario 
I assume the role of Junior Data Analyst working in the marketing analyst team at Atlas Interactive. The marketing director believes the company’s future success depends on maximising Hardcore Players count. Therefore, my team needs to understand how Casual Players and Hardcore Players engage with Shadow City Saga respectively. These insights would enable my team to design a new marketing strategy aimed at converting Casual Players into Hardcore Players. However, Atlas Interactive executives must approve our recommendations, hence the strategy must be backed up with compelling data insights and professional data visualisations.
Ask
Business Task
Devise marketing and product strategies to convert Casual Players into Hardcore Players to maximise the lifetime value of Shadow City Saga.
Analysis Questions
Three questions will guide the future conversion program:
How do Hardcore Players and Casual Players play Shadow City Saga differently?
What behavioral or in-game reward factors would motivate a Casual Player to transition into a Hardcore Player?
How can Atlas Interactive use marketing channels and in-game promotions to convince Casual Players to become Hardcore Players?
Prepare
Data Source
I will use Atlas Interactive’s historical gaming data to analyse and identify trends which can be downloaded from kaggle_dataset. The data has been made available by Creative Commons under this license.
This is public data that can be used to explore how different types of players play Shadow City Saga. But note that data-privacy issues prohibit from using players’ personally identifiable information. This means that we won’t be able to connect in-game purchases to credit card numbers to determine if casual players have purchased multiple premium battle passes and/or the recurring VIP-tier subscription membership.
Data Organization
There is one spreadsheet that contains data such as player id, demographics, game type, engagement time, quantity of purchase, gameplay level and progression. The corresponding column names are: PlayerID, Age, Gender, Location, GameGenre, PlayTimeHours, InGamePurchases, GameDifficulty, SessionsPerWeek, AvgSessionDurationMinutes, PlayerLevel, AchievementsUnlocked, EngagementLevel. 
Process
Spreadsheet is used to work on the dataset and clean it.
Reason:
A spreadsheet can handle up to 10,000,000 cells in Google Sheets. Since Atlas Interactive’s dataset has 520,429 cells (40,033 rows x 13 columns), a spreadsheet is sufficient in handling this volume of data.
Data Exploration & Cleaning
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

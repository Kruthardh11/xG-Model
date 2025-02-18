# xG-Model

 
Let’s dive into one of the most widely used but often less understood metrics in football analysis – xG aka Expected Goals. This metric has revolutionized the wat football analysis is seen. Simply put, xG measures a shot’s quality, highlighting the probability of scoring. 
What exactly are Expected Goals?
It is a metric that assigns a value between 0 and 1 indicating whether that particular shot results in a goal. 
0: No chance of scoring
1: Certain goal

The process:
1. Collecting Data  
To calculate xG, a large amount of data is gathered for every shot taken in a match. Some key details include:  
- Shot Location – Distance and angle from the goal.  
- Play Type – Whether it’s from open play, a set-piece, or a counter-attack.  
- Body Part Used – Whether the shot was taken with the foot, head, or another part.  
- Assist Type – The type of pass that led to the shot (e.g., through ball, cross).  
- Defensive Pressure – How many defenders were near the shooter.  

 2. Building the Model  
A common method to calculate xG is Logistic Regression, since the result of a shot is either a goal (1) or no goal (0).  

The logistic regression formula looks like this:  
 ![lrformula](https://github.com/user-attachments/assets/f6418f0e-a759-4c65-b792-f133a1c5c204)

Where:  
- P(Goal) = Probability of the shot becoming a goal.  
- e = Euler’s number (~2.718).  
- β₀ = The intercept (a baseline value).  
- βᵢ = Weights assigned to different shot factors.  
- xᵢ = The different shot-related variables (e.g., distance, angle).  

 3. Key Factors That Influence xG  
- Shot Distance – Closer shots have a higher chance of scoring.  
- Angle to Goal – Shots from the centre of the goal have a better chance.  
- Type of Shot – Headers usually have lower xG than shots with the foot.  
- Defensive Pressure – More defenders around the shooter reduce the xG.  
- Assist Type – Through balls and crosses often lead to higher xG chances.  

Different data providers use their own models with various factors to estimate xG. If you build your own model, you can experiment with different variables to find the best way to predict scoring probabilities.

How xG is Useful
-	Performance Analysis – Helps determine if a team's results are based on skill or luck.
-	Player Evaluation – Measures a player's finishing ability based on the quality of their chances, often visualized with a shot map.
-	Tactical Insights – Helps coaches understand how often their team creates high-quality chances.

Limitations of xG
-	Data Quality: xG accuracy depends on the detail and reliability of collected data.
-	Model Variations: Different providers use different models; xG values can vary. That is why you might see Sofascore have a shot at .32 xG while on Sky Sports they said it was .25.
-	Contextual Factors: It usually doesn't fully account for player skill, weather conditions, or specific in-game situations.


![compare](https://github.com/user-attachments/assets/f236ec94-21f7-4a25-b6b7-baf6b55acca6)

![lrm](https://github.com/user-attachments/assets/83fd8a4b-d5c4-42b8-b4df-88ed67070b60)

![rfm](https://github.com/user-attachments/assets/fbf62fea-5074-48f8-ba4d-60951871fb9f)



 

 
 


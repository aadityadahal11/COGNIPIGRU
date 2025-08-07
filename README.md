Memory Match Distraction Data
This dataset contains records from a memory matching game where participants flip two cards to find pairs. Various metrics related to their performance and distraction 
levels were recorded over multiple game moves.
Columns:
timestamp: The exact date and time when the move was made.
move_number: The sequential number of the move in the game session.
flipped_card_1: The identifier of the first card flipped in the move.
flipped_card_2: The identifier of the second card flipped.
is_match: Whether the two cards flipped were a correct match (True or False).
reaction_time (sec): Time (in seconds) the participant took to make the move.
off_task_event: Indicates if there was an off-task event (distraction) during the move (1 if yes, 0 if no).
eye_fixation_loss: A measure of how much eye fixation was lost during the move (ranges from 0 to 1, higher means more loss/focus disruption).
distraction_level: A continuous value representing the overall distraction level measured for the move.

Memory Match Frustation Data
This dataset contains data recorded from a memory matching card game, capturing player moves along with associated behavioral and performance metrics. It is designed to 
help model and analyze player frustration during the game.
Key columns:
timestamp: The date and time when the move was made.
move_number: The sequential number of the move in the game.
flipped_card_1 and flipped_card_2: The identifiers of the two cards flipped during the move (e.g., Icon_A, Icon_F).
is_match: A boolean indicating whether the two flipped cards matched (True or False).
reaction_time (sec): The time in seconds taken by the player to make the move.
incorrect_attempts: The cumulative number of incorrect attempts up to that move.
repeated_incorrect: The count of repeated incorrect moves for the same pair or similar pattern.
negative_penalty: A penalty score applied for negative actions or mistakes.
score: The current score after the move, which reflects positive or negative impacts from the player's actions.

Number Sequence Distraction Data
This dataset records user interactions during a number sequence memory game designed to evaluate attention and distraction levels.
Key columns:
user_id: Identifier for each user/player.
round: The game round number for the user.
level: Difficulty level of the sequence presented in that round.
target_sequence: The original sequence of numbers the user is supposed to remember and repeat.
clicked_sequence: The actual sequence of numbers clicked by the user in that round.
response_times (ms): The times taken (in milliseconds) for each click in the sequence.
correct_clicks: Number of clicks that correctly matched the target sequence.
missed_clicks: Number of correct items the user missed.
incorrect_clicks: Number of clicks that were incorrect.
total_time (ms): Total time taken by the user to complete the sequence in that round.
distraction_level: A normalized score (0.0 to 1.0) representing the user’s distraction or attention level during the round; higher values mean more distraction.

Number Sequence Frustation Data
This dataset contains records from a number sequence memory game designed to measure player frustration based on their performance and interactions during each gameplay 
round
Key Columns:
user_id: Unique identifier for each player.
round: The round number in the gameplay session.
level: The difficulty level of the sequence presented in that round.
spawn_time (ms): Time delay before the sequence appears, in milliseconds.
radius (px): The visual size parameter (radius in pixels) of the sequence elements.
target_sequence: The original number sequence the player is supposed to remember.
clicked_sequence: The sequence of numbers the player actually clicked in response.
response_times (ms): Time taken (in milliseconds) for each individual click in the sequence.
correct_clicks: Number of clicks that correctly matched the target sequence.
missed_clicks: Number of elements in the target sequence that the player did not click.
incorrect_clicks: Number of clicks that did not match the target sequence.
total_time (ms): Total time taken by the player to complete the sequence in that round.
frustration_score: A computed numerical score representing the estimated frustration level of the player during that round.

Ball Tracking distraction Data
This dataset contains time-series records of player interactions during a ball-tracking game. It captures various behavioral features that help identify whether the player 
was
distracted during gameplay.
Main Columns:
Sequence_ID: A unique identifier for each game session or sequence.
Timestep: The sequential time step within the game session.
Reaction_Time: The time taken (in seconds) by the player to respond at each time step.
Cursor_Ball_Distance: The distance between the player's cursor and the ball at each time step.
Idle_Time: Amount of idle or inactive time at each step (in seconds).
Error: A binary value indicating if an error occurred at this time step (1 for error, 0 for no error).
Distracted_Label: The label indicating if the player was distracted (1 for distracted, 0 for not distracted) during the entire sequence.
Ball_Speed: Speed of the ball at the current time step.
Level_Difficulty_Index: Numerical index representing the difficulty level of the current game sequence.
Remaining_Level_Time: Remaining time (in seconds) for the current level during the time step.
Target_Accuracy_Gap: The gap between the player’s performance and the target accuracy goal.

Ball Tracking Frustation Data
This dataset contains time-series data collected from a ball-tracking game designed to measure player frustration during gameplay by analyzing their behavioral responses and 
performance.
Key Columns:
Sequence_ID: Unique identifier for each game session.
Timestep: The time step index within each game session.
Reaction_Time: Time (in seconds) the player took to respond at each step.
Cursor_Ball_Distance: Distance between the player's cursor and the ball (in pixels) at each step.
Idle_Time: Duration of inactivity (in seconds) by the player at each step.
Error: Binary flag indicating if an error occurred at that step (1 = error, 0 = no error).
Error_Streak: Number of consecutive errors up to that step.
Reaction_Variability: Variability in reaction times over recent steps.
Recovery_Time: Time taken to recover after an error.
Ball_Speed: Speed of the ball at each step.
Level_Difficulty_Index: Numeric indicator of the difficulty level of the game sequence.
Remaining_Level_Time: Remaining time (in seconds) left in the current game level.
Target_Accuracy_Gap: The difference between the player’s performance and the target accuracy goal.
Frustration_Label: Label indicating whether the player was frustrated during the sequence (1 = frustrated, 0 = not frustrated).

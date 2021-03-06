# Missing-values-extreme
## Background
iRobot has a series of wifi-connected robotic vacuum cleaners available for sale worldwide. These robots
are capable of autonomously navigating a home to vacuum its floors. Upon mission completion, they
send a summary report of the mission to cloud services, where it is processed and stored as a row in a
Postgres database. However, any cleaning mission performed while the robot is not connected to wifi
(either by user's choice or a faulty connection) will not be saved in the database. In addition, there are
occasional periods where cloud services malfunction and no missions are reported, resulting in discrete
periods of data loss.

These robots are programmed with an automatic recharge and resume function, which means that
when the robot detects its battery levels reaching critically low levels, it will navigate back to the
charging dock if available and charge for up to 90 minutes before resuming the mission. In addition, if a
robot becomes stuck on an obstacle in its environment or is manually paused by a button press, it will
cease cleaning for up to 90 minutes before terminating the mission. If the user restarts the mission with
a button press within 90 minutes of the pause, the robot will continue cleaning normally. The number of
minutes spent cleaning, charging, or paused are reported for each mission, as is the mission outcome (a
field describing whether the mission was cancelled, the robot got stuck, the battery died, or the robot
completed the job successfully)

## Task
See the pdf for the question to be solved

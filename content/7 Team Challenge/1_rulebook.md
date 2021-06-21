+++
title = "Rulebook"
weight = 710
chapter = false
pre = "<b>1. </b>"
+++

---

- You will have 5 minutes to fetch as many coins as possible.

  - You can re-run your script any number of times within the alloted period.
  - You are not allowed to make changes to your script midway through a run. You can, however, make changes to your code in between runs.

- There are 5 coin types relevant to this exercise, each made with a different color for easier identification:

  - Bitcoin: red
  - Etherium: grey
  - Litecoin: blue
  - Dash: green
  - Monero: yellow

- The value of a coin is determined by the price shown on [CoinMarketCap](https://coinmarketcap.com/) at the start of the competition.

- At the start of your turn, you will have 5 coins - one of each type - randomly placed around the robot.

  - The coins will be placed such that they are within physical reach of the robot arm.

![Coin placements](/coin-placements.png?classes=border&width=30pc)

- You will have 90 minutes to prepare and test your code for competing in the challenge. Use the application we have built so far as the starting point. Some areas you could work on include:

  - Priortizing the order in which the robot attempts to fetch the coins.
  - Trying out different Rekognition models produced within your team.
  - Experimenting with the confidence threshold parameter for each of the models.
  - Fine-tuning the mathematical formula which converts Rekognition output to physical coordinates.

  > Make sure you start up all of your team's Rekognition models right away as they take several minutes to initialize and get running.

- A coin will be counted towards your final score if it has been picked up and dropped in the deposit area of the robot.

  - If the robot fails to pick up a coin, it will **not** be counted towards your final tally. You can, however, run your script again and re-attempt to fetch the coin.
  - If a coin is dropped after it has been picked up but well before the deposit location, you will receive half of the credit.
  - If a coin rolls around or falls off the table _after_ it has been dropped in the deposit zone, it will still be considered a successful pick up.

  > See how you might use Gazebo to test your code in a virtual environment before running it on the physical arm.

- When you are ready, connect to your team's robot via [Botworks](https://dev.d1aqmxpt45hipw.amplifyapp.com/), and conduct any testing and optimization on the real hardware.

  - The robot assigned to your team will contain your team name in its listing on Botworks.
  - You are free to connect to your team's robot at any point for any duration during the 90-minute preparation window.
  - Only the performance of your script on the real hardware counts; any work done in simulation is just a means to an end.

- Your coins will likely move around and fall off the table as you run tests on the robot hardware. Not to worry; ask the on-site moderators to place your desired number and type of coins around the robot at any point during the preparation window.

  - Send a private message to the on-site moderators with your team name and your desired number/type of coins in the following format. We will place the requested assortment around your robot.

  ```
  Team Red: bitcoin, etherium, litecoin, monero
  ```

  - You can make such requests any number of times from the moderators.

- **Stick to your own hardware.** Booking sessions on another team's robot will lead to instant disqualification.
  > We all can see who is booking a session on which robot. If you accidently book a session you didn't mean to, cancel it immediately.

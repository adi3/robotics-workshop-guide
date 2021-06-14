+++
title = "Rules"
weight = 710
chapter = false
pre = "<b>1. </b>"
+++

---

- You will have 3 minutes to fetch as many coins as possible. You can re-run your script any number of times within those 3 minutes.

- There are 5 coin types relevant to this exercise, each produced with a different color:

  - Bitcoin: red
  - Etherium: gray
  - Litecoin: blue
  - Dash: green
  - Monero: yellow

- The value of a coin is determined by the figures quoted on [CoinMarketCap](https://coinmarketcap.com/) for each cryptocurrency at the start of the competition.

- At the start of your turn, you will have 5 coins - one of each type - randomly placed around the robot.

  - The coins will be placed such that they are within physical reach of the robot arm.

- You will have 90 minutes to prepare and test your code for competing in the challenge. Some areas you could work on include:

  - Priortizing the order in which the robot attempts to fetch the coins.
  - Trying out different Rekognition models produced within your team.
  - Experimenting with the confidence threshold parameter for each of the models.
  - Fine-tuning the mathematical formula and scaling constants which convert Rekognition output to physical coordinates.

- Your coins will likely move around and fall off the table as you run tests on the robot hardware. Not to worry; ask the on-site moderators to place your desired number and type of coins around the robot at any point during the preparation window.

  - Send a private message to the on-site moderators with your team name, and your desired number/type of coins. We will place the requested assortment around your robot.

  ```
  Alpha: bitcoin, etherium, litecoin, monero
  ```

- A coin will be counted towards your final score if it has been picked up and dropped in the deposit area of the robot.

  - If the robot fails to pick up a coin or drops it on the way to the deposit location, it will **not** be counted towards your final tally. You can, however, run your script again and re-attempt to fetch the coin.
  - If a coin rolls around or falls off the table _after_ it has been dropped in the deposit zone, it will still be considered a successful pick up.

- When you are ready, connect to your team's robot via Botworks, and conduct any testing and optimization on the real hardware.

  - You are free to connect to your team's robot at any point for any duration during the 90-minute preparation window.
  - Only the performance of your script on the real hardware counts; the simulation is simply a stepping stone.

- Stick to your own hardware.

  - Do not book sessions on another team's robot. This will lead to instant disqualification. We all can see who is booking session on which robot. If you accidently book a session you didn't mean to, cancel it immediately.

  > See how you might use gazebo to test your code in a virtual environment before testing it on the physical arm.

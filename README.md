# GuardAI
AI For Games - Assignment UE4

The guard AI contains the following functions:
1. Patrolling - The guard AI walks around the map in circles to try to spot the player
2. Chasing - The guard AI chases the players based on the last location of the player
3. Attacking - The guard AI attacks if it is in a certain range of the player. It can also attack and chase at the same time when the player is trying to run away.
4. Searching - The guard AI will search the last three location where the player has been when the guard AI has lost the player out of sight. If he cannot find him he will start patrolling again at the last patrol point

The behaviour tree contains the following decorators:
1. CanSeePlayer/CannotSeePlayer - based on if the guard AI can see the player at that moment
2. HaveBeenChasing - if the guard AI has been chasing the player but cannot see the player (due to the decorator above)

The behaviour tree contains the following services:
1. ChangeNPCSpeed - The speed of the guard AI changes based on the state of the AI (patrolling vs. chasing)
2. PlayerIsInRange - The guard AI will perform a melee attack if it is in a certain range to the player


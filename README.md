
This is a high-fantasy turn-based game utilizing Python's Pygame engine. It uses
pre-rendered 3D images from Blender to simulate animations. The user controls the character or interacts
with the game by using programming languages made specifically for this project. The user inputs actions based
on the syntax specified.

**[Purpose & Goals]**
 - The purpose of this project is to be able to learn how to make programming language rules and syntax in creative way which is creating a game.

**[Technologies used]**
 - **Pygame**: Game logic
 - **Blender**: Assets creation and animation rendering

**[Features]**
 - Turn-based combat controlled through typing programming language syntax made specifically for this project.
 - Pre-rendered assets and animation
 - 


**How does the game work:**
The user starts the game by writing a set of commands using the syntax that is specifically made for this game. The game
has several commands some of these are:

Attack() ---> damages the enemy and uses the stamina resource of the player
Meditate() ----> heals the player's Stamina and HP
Bash() ----> stuns the enemy for certain turns.
Explosion() ----> damages both the player and the enemy
Heal() -----> heals the player's HP and uses the stamina resource of the player
Block() -----> Blocks damage for a certain amount of turns


**The player and the enemies will have randomized stats and skills**
0 - agility 

1 - strength 

2 - intelligence 

3 - HP

4 - physical_damage 

5 - magical_damage 

6 - physical_defence 

7 - magical_defence 

8 - dodge_chance 

9 - perfect_dodge 

10 - crit 

11 - crit_chance 

12 - additional_attack_chance 

13 - block_chance 

14 - block_damage 

15 - block_damage_complete

16 - stamina

17 - [state,state_counter]

 18 - skills

**Primary stats intelligence, strength and agility have its own unique effect on the stats and modifier of each character**

Agility
  -dodge chance
  -crit chance
  -additional attack chance
  
Strength
  -Physical damage
  -block chance
  -Block damage
  -stamina

intelligence
  -magical damage
  -magical_defence
  -additional attack chance

agility 75
strength 13
intelligence 12

HP 109
physical_damage 57
magical_damage 20
physical_defence 33
magical_defence 23
dodge_chance 52
perfect_dodge 15
crit 5
crit_chance 33
additional_attack_chance 15
block_chance 7
block_damage 19
block_damage_complete 1
stamina 131
state None
special skill ['hp_drain()', 'explode()', 'stamina_drain()', 'bash()']
normal skill ['heal()', 'meditate()', 'attack()', 'block()']

Each state has better synergy with different skills. For instance, an explosion deals massive damage for both characters at the cost
of HP. Having more HP means you'll survive the damage dealt to your own.

intelligence increases the explosion's damage but you have to have high hp to use it effectively.



**After typing the command, the player's character and enemy character will start attacking one another automatically turn by turn.**

**player command**
  attack()
  attack()
  meditate()
  attack()

**  flow**
  attack()->enemy_random_attack()->attack()->enemy_random_attack()->meditate()->enemy_random_attack()->meditate2()->enemy_random_attack()->attack()


**  win condition:**
  enemy character runs out of stamina and does not have a skill that restores stamina
  enemy character's hp falls to zero

**  lose condition**
  player character's hp falls down to zero
  player character has no stamina left and has not used any stamina healing move



**enemy behavior:**
enemy also has a behavior that reacts based on the situation presented to them. If the hp is falling down badly, theny the enemy will use healing. If the enemy
stamina is falling down or inssuficient to use any skills or move then it will use a move that regenerate stamina.

  







      

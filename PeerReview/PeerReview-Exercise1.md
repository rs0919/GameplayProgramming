# Code Review for Programming Exercise 1 #
## Description ##

For this assignment, you will be giving feedback on the completeness of Exercise 1.  To do so, we will be giving you a rubric to provide feedback on. For the feedback, please provide positive criticism and suggestions on how to fix segments of code.

You only need to review code modified or created by the student you are reviewing. You do not have to review the code and project files that were given out by the instructor.

Abusive or hateful language or comments will not be tolerated and will result in a grade penalty or be considered a breach of the UC Davis Code of Academic Conduct.

If there are any questions at any point, please email the TA.

## Due Date and Submission Information ##
See the official course schedule for due date.

A successful submission should consist of a copy of this markdown document template that is modified with your peer-review. The file name should be the same as in the template: PeerReview-Exercise1.md. You also need to include your name and email address in the Peer-reviewer Information section below. This review document should be placed into the base folder of the repo you are reviewing in the master branch. This branch should be on the origin of the repository you are reviewing.

If you are in the rare situation where there are two peer-reviewers on a single repository, append your UC Davis user name before the extension of your review file. An example: PeerReview-Exercise1-username.md. Both reviewers should submit their reviews in the master branch.  

## Solution Assessment ##

## Peer-reviewer Information

* *name:* Rohith Saravana 
* *email:* rsaravana@ucdavis.edu

### Description ###

For assessing the solution, you will be choosing ONE choice from: unsatisfactory, satisfactory, good, great, or perfect. Place an x character inside of the square braces next to the appropriate label.

The following are the criteria by which you should assess your peer's solution of the exercise's stages.

#### Perfect #### 
    Can't find any flaws in relation to the prompt. Perfectly satisfied all stage objectives.

#### Great ####
    Minor flaws in one or two objectives. 

#### Good #####
    Major flaw and some minor flaws.

#### Satisfactory ####
    Couple of major flaws. Heading towards solution, however did not fully realize solution.

#### Unsatisfactory ####
    Partial work, not really converging to a solution. Pervasive Major flaws. Objective largely unmet.


### Stage 1 ###

- [x] Perfect
- [ ] Great
- [ ] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

#### Justification ##### 
When the right arrow is pressed, the captain moves right in the same way that he moves left. Also the captain sprite flips orientation so he is facing right as he is moving right. The implementation is correct, because the CaptainController script was updated so that when the right arrow is pressed, the moveRight script is called which adds positive velocity to the player character.

### Stage 2 ###

- [x] Perfect
- [ ] Great
- [ ] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

#### Justification ##### 
All Three pirate behaviors were implemented correctly. For the slow worker, the script randomly generates a work duration of 20 to 40 seconds and it instantiates the appropriate prefab every 8 seconds. For the normal worker, the work duration is randomly generated from 10 to 20 seconds and a prefab spawns every 4 seconds. For the fast worker, the work duration is randomly generated from 5 to 10 seconds, and a prefab spawns every 2 seconds. Also, for all 3 scripts, the Execute function is responsible for instantiating the prefab and correctly returns true if the pirate is working. If the pirate has worked for the work duration period, then it will no longer spwan objects and the function returns false, so the pirate is now exhausted.

### Stage 3 ###

- [ ] Perfect
- [x] Great
- [ ] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

#### justification ##### 
In the Motivate function, the number 1, 2, or 3 is randomly generated. Each of the different pirate behaviors (slow, normal, fast) has its own number and it is instantiated if the number is called. In the game, if the captain motivates an exhausted pirate, they will be assigned one of these behaviors and work for the appropriate duration. If the captain motivates them while they are still working, then the pirate behavior will reset and be reassigned another random behavior. The Motivation function correctly uses the Object.Instantiate(ScriptableObject.CreateInstance<SlowWorkPirateCommand>()); code to create a new instance of IPirateCommands.

The only error I noticed was that the Start function calls all three instances of the pirate behavior consecutively. Everytime the game starts, the pirates always start with the fastworker behavior. If this was the intended goal, then the two previous lines (add link?) should be removed and you only need to instantiate the fastWorker behavior. If this was not intended and it is supposed to be random, then the code block used in the Motivate function should also be used in the Start function to give the pirates a random behavior when the game starts.

### Stage 4 ###

- [ ] Perfect
- [ ] Great
- [x] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

#### justification ##### 
The fire2 input was used to implement a jump movement for the Captain. The MoveJump script is called everytime time fire2 (left alt) is pressed. The MoveJump script adds positive vertical velocity to the Captain so that he jumps in the air. tThe captain can jump in place, but can also allows jump while running left or right. When the captain reaches its max height, he will fall back to the ground, like how a normal jump works. The fire2 also only works when the key is initally pressed, holding it or letting go does not affect the jump. Also the captain is bounded by the floor and ceiling and can not jump past the game worlds
    
One major flaw with how the jump was implemented is that it does not check whether the Captain is on the ground or not when he jumps. This means that the Captain can jump while he is still in the air. If you spam the fire2 input, the Captain can jump up unlimitied amounts of times, essentially allowing him to fly until he hits the top of the level, which is not the intended behavior. To fix this, the MoveJump script would have to check if the Captain's position was on the ground, before adding positive vertical velocity to the Captain's rigidBody. 

## Code Style ##

### Description ###
Check the scripts to see if the student code follows the .Net style guide.

If there are sections that don't adhere to the style guide, please peramlink the line of code from Github and justify why the line of code has infractions of style guide.

It should look something like this:

* [description of infraction](https://github.com/dr-jam/ECS189L) - this is the justification.

Here is an example of the permalink drop down on Github.

![Permalink option](../images/permalink_example.png)

Here is another example as well.

* [I go to Github and look at the ICommand script in the ECS189L repo!](https://github.com/dr-jam/ECS189L/blob/1618376092e85ffd63d3af9d9dcc1f2078df2170/Projects/CommandPatternExample/Assets/Scripts/ICommand.cs#L5)

### Code Style Review ###

#### Style Guide Infractions ####

#### Style Guide Exemplars ####

## Best Practices ##

### Description ###

If the student has followed best practices (Unity coding conventions from the StyleGuides document) then feel free to point at these segments of code as examplars. 

If the student has breached the best practices and has done something that should be noted, please add the infracture.

This should be similar to the Code Style justification.

* [description of infraction](https://github.com/dr-jam/ECS189L) - this is the justification.

### Best Practices Review ###

#### Best Practices Infractions ####

#### Best Practices Exemplars ####

# Peer-Review for Programming Exercise 2 #

## Description ##

For this assignment, you will be giving feedback on the completeness of assignment two: Obscura. To to do so, we will be giving you a rubric to give feedback on. For the feedback, please give positive criticism and suggestions on how to fix segments of code.

You only need to review code modified or created by the student you are reviewing. You do not have to review the code and project files that were given out by the instructor.

Abusive or hateful language or comments will not be tolerated and will result in a grade penalty or be considered a breach of the UC Davis Code of Academic Conduct.

If there are any questions at any point, please email the TA.   

## Due Date and Submission Information
See official course schedule for due date.

A successful submission should consist of a copy of this markdown document template that is modified with your peer-review. The file name should be the same as it is in the template: `CodeReview-Exercise2.md`. You also need to include your name and email address in the `Peer-reviewer Information` section below. This review document should be placed into the base folder of the repo you are reviewing in the master branch.

If you are in the rare situation where there are two peer-reviewers on a single repository, append your UC Davis user name before the extension of your review file. An example: `CodeReview-Exercise2-username.md`. Both reviewers should submit their reviews in master branch.  

# Solution Assessment #

## Peer-reviewer Information

* *name:* Rohith Saravana 
* *email:* rsaravana@ucdavis.edu

### Description ###

For assessing the solution, you will be choosing ONE choice from: unsatisfactory, satisfactory, good, great, or perfect.

The break down of each of these labels for the solution assessment.

#### Perfect #### 
    Can't find any flaws with the prompt. Perfectly satisfied all stage objectives.

#### Great ####
    Minor flaws in one or two objectives. 

#### Good #####
    Major flaw and some minor flaws.

#### Satisfactory ####
    Couple of major flaws. Heading towards solution, however did not fully realize solution.

#### Unsatisfactory ####
    Partial work, not converging to a solution. Pervasive Major flaws. Objective largely unmet.


___

## Solution Assessment ##

### Stage 1 ###

- [x] Perfect
- [ ] Great
- [ ] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

___
#### Justification ##### 
The position lock camera is implemented so that the player character is always in the center of the screen. Regardless of the direction, the camera follows the player and stays on top of them. The camera also matches the speed of the player and will keep the player centered even if they are going faster. Enabling Draw Logic draws a cross on the center of the screen, which aligns with the player, so that they are always in the middle of the cross. Disabling Draw Logic removes this cross.

___
### Stage 2 ###

- [ ] Perfect
- [x] Great
- [ ] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

___
#### Justification ##### 
The frame autoscroll camera is implemented so that the camera moves at a constant speed to the right while the player is within the camera box. If the player goes to the right of the box, the camera moves at the same speed as the player. If the player goes to the left of the camera box, then it stays at the left edge at moves at the same speed as the camera. The player can move freely on the y-axis and the camera will follow it if it goes past the camera box. The only issue with this camera is that if the player is on the left edge of the camera box, it will lock to the middle left of the camera box. Even if the the player is at the top left or bottom left, they will be moved to the middle left. This creates a jarring effect, in which the player sometimes seems to teleport.

___
### Stage 3 ###

- [ ] Perfect
- [ ] Great
- [ ] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

___
#### Justification ##### 
Write Justification here.

___
### Stage 4 ###

- [ ] Perfect
- [ ] Great
- [ ] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

___
#### Justification ##### 
Write Justification here.

___
### Stage 5 ###

- [ ] Perfect
- [ ] Great
- [ ] Good
- [ ] Satisfactory
- [ ] Unsatisfactory

___
#### Justification ##### 
Write Justification here.
___
# Code Style #


### Description ###
Check the scripts to see if the student code adheres to the dotnet style guide.

If there are sections that don't adhere to the style guide, please peramlink the line of code from Github and justify why the line of code has infractured the style guide.

It should look something like this:

* [description of infraction](https://github.com/dr-jam/ECS189L) - this is the justification.

Please refer to the first code review template on how to do a permalink.


## Code Style Infractures ##

___
#### Put style guide infractures ####

___

# Best Practices #

### Description ###

If the student has followed best practices (Unity coding conventions from the StyleGuides document) then feel free to point at these segments of code as examplars. 

If the student has breached the best practices and has done something that should be noted, please add the infracture.


This should be similar to the Code Style justification.

## Best Practice observations ##

___
### Put best practice observations here ###
___

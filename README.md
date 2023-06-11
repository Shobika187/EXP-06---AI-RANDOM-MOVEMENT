# EXP-06---AI-RANDOM-MOVEMENT
## AIM:
To implement AI concept to the actor for a random movement.
## ALGORITHM:
### STEP 1: Create a Character Blueprint:
```
i)In the Content Browser, right-click in the desired folder
ii)Select Create Basic Asset > Blueprint Class.
iii)Choose the appropriate parent class for your AI character (e.g., Character or Pawn).
iv)Name the Blueprint (e.g., "AICharacter") and click Create.
```
### STEP 2: Create a Blackboard:
```
i)In the Content Browser, right-click in the desired folder.
ii)Select Create Basic Asset > AI > Blackboard.
iii)Name the Blackboard (e.g., "AIBlackboard") and click Create.
```
### STEP 3: Open the Behavior Tree editor:
```
i)In the Content Browser, find the Blackboard asset you just created.
ii)Right-click the Blackboard asset and select Create > Behavior Tree.
iii)Name the Behavior Tree (e.g., "AIBehaviorTree") and click Create.
iv)Double-click the Behavior Tree asset to open it in the Behavior Tree editor
```
### STEP 4: Create Behavior Tree nodes:
```
i)In the Behavior Tree editor, right-click in the graph and search for and add the following nodes:
ii)"Selector" node: Controls the execution of child nodes.
iii)"Service" node: Monitors and updates values in the Blackboard.
iv)"Sequence" node: Executes child nodes in sequential order.
v)"Random" decorator: Randomly selects a child node to execute.
vi)"Move To" task: Moves the AI character to a specified location.
vii)Connect the nodes to create the desired behavior flow.
viii)Connect the nodes to create the desired behavior flow. For example:
ix)Connect the Random decorator to the Sequence node.
x)Connect the Move To task to one of the child nodes of the Random decorator.
```
### STEP 5: Set up the Blackboard:
```
i)Open the AIBlackboard asset.
ii)In the Blackboard editor, define the necessary keys for storing data, such as:
iii)Vector keys: for storing target locations.
Bool keys: for storing condition flags.
iv)Save the AIBlackboard asset.
```
### STEP 6: Set up the AI character Blueprint:
```
i)Open the AICharacter Blueprint.
ii)In the Blueprint editor, find the Components panel.
iii)Add an AI Controller component to the AICharacter Blueprint.
iv)In the Details panel, under the AI Controller section, set the AIController Class to the desired AI controller class (e.g., AIController).
v)Save the AICharacter Blueprint
```
### STEP 7: Set the AI controller and behavior tree:
```
Open the AIController Blueprint.

i)In the Blueprint editor, locate the Event Begin Play event.

ii)Drag off the execution line and search for "Possess".

iii)In the Possess node, select the AICharacter Blueprint you created.

iv)Drag off the AICharacter reference and search for "Use Blackboard".

v)Connect the output of the Use Blackboard node to the AIController's Blackboard property.

vi)In the Blackboard property, select the AIBlackboard asset you created.

vii)Drag off the AICharacter reference again and search for "Run Behavior Tree".

viii)Connect the output of the Run Behavior Tree node to the AIController's Behavior Tree property.

iX)In the Behavior Tree property, select the AIBehaviorTree asset you created.

x)Save the AIController Blueprint.
```

### STEP 8: Set up the NavMesh and boundaries:
```
i)Place a NavMeshBoundsVolume in your level to define the AI character's movement boundaries.

ii)Adjust the size and position of the NavMeshBoundsVolume to cover the desired playable area
```
## OUTPUT
### AI PLAYER MESH:
![image](https://github.com/Shobika187/EXP-06---AI-RANDOM-MOVEMENT/assets/94508142/cab18da5-39b6-49d1-a4ea-ffd9c638e109)
### AI Backboard for Key Creation:
![image](https://github.com/Shobika187/EXP-06---AI-RANDOM-MOVEMENT/assets/94508142/02c67eb9-08e1-4ff6-aa54-34aee22c4e96)
### Behaviour Tree:
![image](https://github.com/Shobika187/EXP-06---AI-RANDOM-MOVEMENT/assets/94508142/0ff0e318-be04-49b5-adcf-a79ea4ea7889)

### Blackboard Event Graph:
![image](https://github.com/Shobika187/EXP-06---AI-RANDOM-MOVEMENT/assets/94508142/9f803af0-3aef-43e5-8dde-96019b6c344a)

### Game Nav-Mesh Bound Volume:
![image](https://github.com/Shobika187/EXP-06---AI-RANDOM-MOVEMENT/assets/94508142/06e4f1e1-284e-4da8-956b-2124d3d877df)


### In Play Mode:
![image](https://github.com/Shobika187/EXP-06---AI-RANDOM-MOVEMENT/assets/94508142/9bb2b04c-9cb6-4247-927f-67decb21a74a)
### RESULT:
Thus, the AI concept to the actor for a random movement is implemented.

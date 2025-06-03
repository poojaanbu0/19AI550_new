# Ex.No: 4  Create a player Movement Script in unity 
### DATE: 11.04.2025                                                                          
### REGISTER NUMBER : 212222240072
### AIM: 
To write a program to create a player movement in unity.
### Algorithm:
1. Create a New Unity Project by Open the  Unity Hub and create a new 3D Project,Name the project (e.g., PlayerMovement).
2. Create the Moving Object
   In the Hierarchy, right-click → 3D Object → Capsule (or Sphere).
   Rename it to Player 
4. Adding the Player Movement Behavior Script
   Create the Script-In the Project Window, go to the Assets folder.
   Right-click → Create → C# Script.
5. Write a script for player behavior and save it
6. Attach the Script
   Select player in the Hierarchy - Drag & Drop the playerBehavior script onto the Inspector Panel.
7. Run the game 
8. Stop the program
    
### Program:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Player_movement : MonoBehaviour
{
    public float speed = 5.0f;

void Update()
{
    float xdir = Input.GetAxis("Horizontal") * speed * Time.deltaTime;
    float zdir = Input.GetAxis("Vertical") * speed * Time.deltaTime;

    transform.Translate(xdir, 0, zdir);
}
}

```
### Output:

![423383693-eaa695c2-16eb-4fbf-a4be-0a7fac41be1b](https://github.com/user-attachments/assets/2e90bdb8-7f2d-4740-b083-214c9381b042)

![423383738-fd4fcb60-2da3-416e-946c-c43d366d42ae](https://github.com/user-attachments/assets/300f6b0d-edbd-486d-9399-63b0dda825c8)

![423383788-98453693-1187-40c0-ad84-a604332389fb](https://github.com/user-attachments/assets/f5c7f28e-1ba7-4517-9d79-4003674eb9bb)

![423383874-b13eabc2-5dd7-49d2-9a1e-f1501a9c54ac](https://github.com/user-attachments/assets/33eff142-7936-449e-b772-23722630241c)





### Result:
Thus the simple movement behavior was implemented successfully.

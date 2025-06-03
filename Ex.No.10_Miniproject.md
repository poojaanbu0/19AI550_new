# Ex.No: 10   Implementation of 2D/3D game - Escape from the Falling Object Game                     
### DATE: 16.05.2025                                       
### REGISTER NUMBER : 212222240072
### AIM: 
To develop a Escape from the Falling Object Game in Unity

### Algorithm:
```
1. Create a new Unity project.
2. Add a Player GameObject to the scene.
3. Add a FallingObject GameObject to the scene.
4. Attach the PlayerController script to the Player GameObject.
5. Attach the FallingObject script to the FallingObject GameObject.
6. Set the Player GameObject's tag and add a Collider2D (if needed).
7. Set the Ground GameObject with tag "Ground" and add a Collider2D with IsTrigger enabled.
8. In the PlayerController script, read horizontal input and move the player each frame (in Update).
9. In the FallingObject script, move the object downwards each frame and check for collision with the ground using OnTriggerEnter2D.
10. If the falling object collides with the ground, destroy the player object.
```  
### Program:
#### FallingObject.cs
```
using UnityEngine;

public class FallingObject : MonoBehaviour
{
    public float fallSpeed = 1f;

    void Update()
    {
        transform.position += new Vector3(0, -fallSpeed * Time.deltaTime, 0);
    }

    void OnTriggerEnter2D(Collider2D other)
    {
        if (other.gameObject.CompareTag("Ground"))
        {
            Destroy(gameObject); // Destroy the object when it hits the ground
        }
    }
}

```

#### PlayerController.cs
```

using UnityEngine;

public class PlayerController : MonoBehaviour
{
    public float speed = 5f;

    void Update()
    {
        float move = Input.GetAxis("Horizontal"); // Get left/right key input
        transform.position += new Vector3(move * speed * Time.deltaTime, 0, 0);
    }
}
```

### Output:
![445699345-f0ae77b1-f643-41ef-a604-3b00b31f9b10](https://github.com/user-attachments/assets/be0e85be-c1af-4aed-afbc-51c846c48929)

![445699402-6213cc1e-28f4-49bf-a996-a848118888ce](https://github.com/user-attachments/assets/683c9463-93a9-4455-ac4f-fef5044ee941)

![445699444-1495f1f2-34bd-4138-9d7a-fbe287956aea](https://github.com/user-attachments/assets/18a212a1-4e89-4ceb-94f0-83cf68f6368c)

### Result:
Thus the game Escape from the Falling Object Game was developed using Unity.

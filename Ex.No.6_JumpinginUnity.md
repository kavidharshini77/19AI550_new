# Ex.No: 6  Implementation of Jumping  behaviour- Unity
### DATE:  29.07.26                                                                          
### REGISTER NUMBER : 212225240069
### AIM: 
To write a program to simulate the process of jumping in Unity.
### Algorithm:
```
1. Create a new 3D Unity project
2. Add a Plane
3. Right-click Hierarchy → 3D Object → Plane → Rename to Ground
4. Add a Cube (Player)
5. Right-click Hierarchy → 3D Object → Cube → Rename to Player
6. Set Position: (0, 0.5, 0)
7. Add a Rigidbody to the Player
8. With the Player selected: Inspector → Add Component → Rigidbody
9. Set Constraints > Freeze Rotation X, Z (optional for stability)
10.Create the Jump Script and Apply the Script Player
11.Run the game
Press Play
Press Spacebar to jump
Your cube should only jump when touching the ground
```
###
**Program **
```
using UnityEngine;

public class PlayerJump : MonoBehaviour
{
    private Rigidbody rb;
    public float jumpForce = 5f;
    
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space) )
        {
            rb.AddForce(Vector3.up * jumpForce, ForceMode.Impulse);
            
        }
    }

   
}
```
### Output:
<img width="1920" height="1080" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/bcd85e14-5585-4b64-b5d2-27d9895352b4" />

<img width="1920" height="1080" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/922df7f9-e574-462f-863f-b1214fd6c25c" />

### Result:
Thus the simple jumping behavior was implemented successfully.

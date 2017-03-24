# SmoothLookAt

Put this in your move target.

```
var targetObj : GameObject;
var speed : int = 5;
 
function Update(){
var targetRotation = Quaternion.LookRotation(targetObj.transform.position - transform.position);
     
// Smoothly rotate towards the target point.
transform.rotation = Quaternion.Slerp(transform.rotation, targetRotation, speed * Time.deltaTime);
}
```




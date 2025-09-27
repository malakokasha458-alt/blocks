extends CharacterBody2D
var speed=100
func _physics_process(delta: float) -> void:
	move_and_slide()
	if Input.is_action_pressed("right"):
		velocity.x = speed
	elif Input.is_action_pressed("left"):
		velocity.x = speed*-1
	else : 
		velocity.x = 0 
	if not is_on_floor() :
		velocity.y+=9
	if Input.is_action_just_pressed("up") and is_on_floor():
		velocity.y-= 700
pass

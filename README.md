# Generic Animation State Behaviour
A Unity package for generic animation state behaviour class. Useful if you find Unity's built in Animation Event hard to work with.

# Classes
## Animation Event
Used for storing the Enum type and the Event that have to be triggered.

## Animation Event State SO
Used for storing the Enum type and when the animation Event is triggered.

## Animation Event State Behaviour
Used to raise the Event of the animation to Animation Event State Reciever class. Attach this component to an Animation State.

## Animation Event State Reciever
Used to invoke the Event raised by Animation Event State Behaviour class. Attack this component to a gameobject with an Animator component.

# How to Use
### Step 1
Create an Enum for your Animation states.
### Step 2
Create 3 new classes that inherits from AnimationEventStateSo, AnimationEventStateBehaviour, and AnimationEventStateReciever respectively. Change the type T Generic to the Enum you just created. You can extend the classes with new methods or modify existing methods from the parent class. But you can also leave it empty if you don't want to add anything.

Don't forget to add CreateAssetMenu Attribute to the new AnimationEventStateSo class you created.
### Step 3
Create Scriptable Objects of your AnimationEventStateSo. Choose the Animation state from the Enum field, and when to trigger the Event in the float field.
### Step 4
Open your Animator window, and choose a State. Attach your AnimationEventStateBehaviour component. Add your AnimationEventStateSo Scriptable Objects to the AnimationEventStateBehaviour fields.
### Step 5
Open your gameobject with the Animator component. Attach your AnimationEventStateReciever component. Choose the Animation state from the Enum field, and add the Event you want to trigger.

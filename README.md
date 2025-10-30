# Generic Animation State Behaviour
A Unity package for generic animation state behaviour class. Useful if you find Unity's built in Animation Event hard to work with.

# Classes
## Animation Event
<img width="573" height="212" alt="Animation Event" src="https://github.com/user-attachments/assets/93317271-e621-41dc-91e7-2934c3f01ba9" />

Used for storing the Enum type and the Event that have to be triggered.

## Animation Event State SO
<img width="913" height="165" alt="Animation Event State SO" src="https://github.com/user-attachments/assets/1e725859-2995-4fcf-aefa-d08d3abcc64e" />

Used for storing the Enum type and when the animation Event is triggered.

## Animation Event State Behaviour
<img width="1337" height="492" alt="Animation Event State Behaviour" src="https://github.com/user-attachments/assets/7bbc11ba-e09a-4611-bb54-fa32ed0d05d7" />

Used to raise the Event of the animation to Animation Event Reciever class. Attach this component to an Animation State.

## Animation Event Reciever
<img width="1286" height="283" alt="Animation Event Reciever" src="https://github.com/user-attachments/assets/7a04747d-0427-4bf4-a49b-3886256feb28" />

Used to invoke the Event raised by Animation Event State Behaviour class. Attack this component to a gameobject with an Animator component.

# How to Use
### Step 1
<img width="380" height="301" alt="Step 1" src="https://github.com/user-attachments/assets/95b281aa-2e77-4a01-a0ba-ff8f729f4ef6" />

Create an Enum for your Animation states.
### Step 2
<img width="949" height="82" alt="Step 2a" src="https://github.com/user-attachments/assets/9bd26911-a5bb-4b41-8b79-ae5bf254dc96" />
<img width="1096" height="37" alt="Step 2b" src="https://github.com/user-attachments/assets/d3913025-d957-41a7-b55f-1ee8baaec500" />
<img width="981" height="35" alt="Step 2c" src="https://github.com/user-attachments/assets/7299cc7a-d367-4885-bcc5-d4fc32ec0277" />

Create 3 new classes that inherits from AnimationEventStateSo, AnimationEventStateBehaviour, and AnimationEventReciever respectively. Change the type T Generic to the Enum you just created. You can extend the classes with new methods or modify existing methods from the parent class. But you can also leave it empty if you don't want to add anything.

Don't forget to add CreateAssetMenu Attribute to the new AnimationEventStateSo class you created.
### Step 3
<img width="586" height="151" alt="Step 3a" src="https://github.com/user-attachments/assets/dd3398a5-5710-43d1-9ef0-99dcd426ee9d" />
<img width="593" height="156" alt="Step 3b" src="https://github.com/user-attachments/assets/a25bab9b-fb2a-4311-aa34-5087415b45de" />

Create Scriptable Objects of your AnimationEventStateSo. Choose the Animation state from the Enum field, and when to trigger the Event in the float field.
### Step 4
<img width="590" height="561" alt="Step 4" src="https://github.com/user-attachments/assets/ccce3108-4755-40b6-b23b-91dcf39f1583" />

Open your Animator window, and choose a State. Attach your AnimationEventStateBehaviour component. Add your AnimationEventStateSo Scriptable Objects to the AnimationEventStateBehaviour fields.
### Step 5
<img width="595" height="791" alt="Step 5" src="https://github.com/user-attachments/assets/dee0b9fd-5f89-4c77-bfda-0bd68b8412e7" />

Open your gameobject with the Animator component. Attach your AnimationEventReciever component. Choose the Animation state from the Enum field, and add the Event you want to trigger.

# How to Download
Click the green "Code" button on the top. Click "Download ZIP". Extract the ZIP file, and drag the "Generic Animation State Behaviour.unitypackage" to your Unity Editor.

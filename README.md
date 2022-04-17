# Challenge 2 - 3D Painting
### 1. The Canvas that allows you to change the shape on the pedestal follows the camera.
Bij het gameobject Canvas_Pedestal in de Canvas component de property Render Mode veranderen van screen space naar world space.

### 2. The toggled ray and palette canvas are tracking the opposite hands.
Bij het gameobject XR Rig stonden de refrences bij de XR Controller van de linkerhand ook allemaal op rechts. Dit aanpassen naar links loste het probleem op.

### 3. The paint brush activation is backwards, starting when the trigger is released and stopping when it’s pressed.
Bij het gameObject Paintbrush was bij de OnActivate de methode EndTrail gelinked en bij de On Deactivate de StartTrail, dit moet andersom zijn.

### 4.  The medium brush size button turns invisible when pressed and makes the trail gigantic.

De alpha (transparency) value van de medium button bij pressed color stond op 0 en bij de andere op 255. De trail width bij onclick werd op 0.25 gezet terwijl large maar 0.05 is, deze waarde is aangepast naar 0.025 zodat het tussenin zit.

### 5.  The paint brush sound effect stays the same, regardless of how far it is from you.
The paint brush sound should be at full volume close to your face, but about 50% volume when your arm is outstretched

Gebruik maken van een linear rollof met max distance 2 zodat er op 1m 50% is.

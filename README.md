TUTORIAL - AS2 GLB Model Viewer with re-color functionality. 
_______________________________________________________________________________________________________________________________________________
DETAILS:

The AS2 GLB Model Viewer is a web utility that allows .glb models to be viewed in a browser, and then re-colored using the .glb file format's 
material variant system. This is very helpful if you would like to quickly apply alternative colors to an existing model.
<img width="1000" alt="image" src="https://github.com/user-attachments/assets/7f4f9362-411a-4145-aa83-4622bec92ebf" />

_______________________________________________________________________________________________________________________________________________
PREREQUISITES:

1) A modern web browser, with support for three.js enabled (this should be enabled by default in most browsers).
2) If you would like to see newly created material variants in Blender, then you'll need to first confirm two things are enabled in the 
'Preferences' section for Blender. Please refer to the screenshot below, and ensure that the checkbox for: '.gltf 2.0 format' is checked, and 
also that the ''Material Variants' checkbox is checked. You will need to restart Blender after enabling either of these.   
![image](https://github.com/user-attachments/assets/6893e379-b496-498f-a798-98e72438bdb4)

_______________________________________________________________________________________________________________________________________________
SETUP STEPS:

STEP A) Pull down the AS2 repo to a desired directory on your local machine.

STEP B) You should see the 'SAMPLE.html' file in the new directory. Double click it to see it in your default browser. This is a template to 
test your browser with and ensure there are no problematic settings. 

STEP C) Test by clicking the 'Upload Model' button in the top left hand side of the browser, and then choosing either:
  - A .glb 3d model of your own, or
  - The sample .glb model provided in the 'SAMPLE_MODEL' directory named: 'FISH_SCULPTURE.glb'.

STEP D) If you've used the provided sample .glb model, it should look like this:
<img width="1000" alt="image" src="https://github.com/user-attachments/assets/8cc1f20a-15b6-4381-a470-e9079e273aa4" />

STEP E) The setup should be complete now. You may now re-name the 'SAMPLE.html' file to whatever you would like and continue building futher
features of your own.

_______________________________________________________________________________________________________________________________________________
UI EXPLAINED:

BUTTONS:

Button #1: Import .glb Model:

Use: This allows a user to select a .glb model on their local machine, and then upload it so it can be seen in the AS2 app and color swapped.

<img width="140" alt="image" src="https://github.com/user-attachments/assets/01cce6e6-c0dd-4556-a492-ee5e02418ae3" />


Button #2, #3, #4:

Use: These three buttons allow a user to specify colors on a .glb mode's material, and then choose replacement colors to be applied as 
material variants. All three buttons work the same. 




Button #5: Reset Camera:

Use: This will allow you to revert the camera back to it's original position. 

<img width="240" alt="image" src="https://github.com/user-attachments/assets/c9219246-9f3b-46f1-8210-dd6ae6722dfb" />

 


Button #6: Export Model + Material Variants:

Use: This allows the user to export the newly color swapped .glb model to a desired directory on their local machine. Please note that if you
intend to then open the model in Blender, than you need to enable the two settings from the 'PREREQUISITES' section near the top of this guide.
Without that functionality, Blender will not show you material variants, and it will not appear as if any are present.

_______________________________________________________________________________________________________________________________________________
TROUBLESHOOTING:

A) Color swaps work best when circumstances are simple; as such, changing the color of a vase from blue to red is more simple than changing a
skin texure from one color to another. This is because some colors are constant and truly uniform, while others only appear to be uniform, and
are instead made up of hundreds of slightly different colored pixels (such as a skin tone). Similar to the paint bucket tool in Photoshop, a 
tolerance value determines the degree to which the color swap functionality can extend itself. If it's too high, far more colors can be 
swapped than intended, and if it's too low, then only one or two pixels may be selected. A slider for the tolerance would be a prudent feature
for later, but currently falls outside the scope of this app.

B) Not all models are created equally. Some AI asset generators produce unreliable or empty .glb models, as such, if you notice distortions on 
an imported model, then open it in Blender or 3ds Max and confirm if the defect is also present there.

C) Very large models can be problematic, so ensure you're keeping your models to less than 20 MBs. Depending on your local device's capabilities, 
you may be able to upload larger models than that, but color swap operations are likely to be slow.

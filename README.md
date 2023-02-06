# CoRegi-Muitispectral-HE
This application implements the manual or automatic alignment of H&E images and their corresponding multispectral images. 

It is one of the steps of  Goossens, P., Lu, C., Cao, J., Gijbels, M. J., Karel, J. M., Wijnands, E., ... & Biessen, E. A. (2022). Integrating multiplex immunofluorescent and mass spectrometry imaging to map myeloid heterogeneity in its metabolic and cellular context. Cell Metabolism, 34(8), 1214-1225.

Image Processing Toolbox is required


Tutorial

a.	Download and install the ‘CoRegi-Muitispectral-HE.mlappinstall’ app in MATLAB; Make sure you have installed the 'Image processing Toolbox’

b.	Open the app; In the pop-up window, click “load” to select a H&E image file (H&E) and the fluorescently imaged nuclear staining (7AAD) from the same section; 

c.	Stay in the ‘manually’ panel to align the image manually by selecting landmarks on both fluorescent image and H&E image, or change to ‘auto’ panel for alignment automatically.

d.	For the manual registration, select the “selectpoint”, and click ‘run’, a new window will show the fluorescent and brightfield images next to each other. Click to place a crosshair on a recognizable landmark in one image and select the corresponding point in the other. Repeat this step several times until minimally 5 landmarks, spread over the field of view, are assigned. Next, click the icon depicting two stars to let the script predict additional points. Adjust these manually if necessary.

e.	Close this pop-up window and the main window will now show a merged image. When sufficiently overlapping, save the new H&E image (HE.jpg), transformation matrix (tform.mat), or landmarks location by selecting check boxes  in the ‘save panel’. 

f.	With the landmark file or tform data, when you need to perform image alignment for the same images next time, you can load the landmark file or tform.mat into the app by clicking ‘alignwithpoint’ or ‘alingwithtform’, instead of having to select the landmark again. 

g.	You can also align H&E image and 7AAD image automatically by switching to the ‘auto’ panel. Next, adjust the parameter of image processing for both H&E and 7AAD image. Click ‘processing’ button, processed images will be shown on the window. Click ‘reigstration’ and wait for a few seconds, the image after reregistration will be visualized on the window (Depending on the computer configuration, image size and resolution, the running time will be different, so please be patient.).

h.	Save the H&E image after alignment and transformation matrix data by clicking ‘save’ if you are satisfied with the result. If not, adjust the parameter for a better automatic alignment, or select manual registration.


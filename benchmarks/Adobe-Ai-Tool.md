
 
I have been using either the line tool or the pen tool to create property boundary lines for 15 years. Today I went to add some lines to a few images and strange things are happening. Where as I have always just held the control key and clicked the first placement, the second etc till I created all the lines. Now, when I go to click the second line, the the anchor point just moves. If I try to work around by just clicking another area after the first line is created, I have to go to another area, as the first anchor points are still active. If I create all the lines through the workaround (not ideal), the when going to flatten the image, all the lines disapear, and there is no option to bring them to the front. The only way to flatten the image and still have lines is to "set shape layer to stroke"
 
**DOWNLOAD ✔ [https://kneedacexbrew.blogspot.com/?d=2A0OWi](https://kneedacexbrew.blogspot.com/?d=2A0OWi)**


 
The same happens to me when I go to rasterize the lines. I'm already a bit bitter about them graying out (might as well say "removed") the pixel format, but can work with shapes and path with ease because like you, I've been working with those features for a very long time. Sometimes when I want to thicken the stroke lines, nothing happens.
 
Adobe remove line weight and changed how you size arrowheads. The only shape layers the Line tool can create are arrowhead shapes. If you stroke the arrowhead shapes you can get a single stroke or a double stroke line between the Arrowheads however the arrowheads will also be stroke and portraits their intended marks.
 
A path has no fill or stroke, similar to a selection. You can stroke it in the Paths panel, which will put pixels on the current layer. Those pixels are not connected to the path. If you need to redraw, first erase the pixels and edit the path, then stroke the path again.

Sounds like using the pen tool to create boundary lines on a property is not at all the way to go. The line tool works, but one can't just click on the end of the last line drawn anymore, as that point is still an anchor point now and will not allow a new line to be drawn, but only to adjust the placement of that anchor point. Not as accurate and easy as it once was, but doable. Thanks for your input.
 
The Line tool is broken in 2021 and even if it was not you cans not connect lines together like the pen tool. The line tool creates a single line segment. Connecting line with the line tool is hit or miss. All they need does as you wrote is stroke the path they created with the pen tool in the image or into new empty top layer.
 
It would be great to use tyhe pen tool to simply create the path. What I don't understand is how to turn that path into a line. I looked at the tutorial Jane linked to, and tryed to understand what Jane said
 
"A path has no fill or stroke, similar to a selection. You can stroke it in the Paths panel, which will put pixels on the current layer. Those pixels are not connected to the path. If you need to redraw, first erase the pixels and edit the path, then stroke the path again."
 
But I don't follow how to translate that into practice. I'm and old Photographer now, using Photoshop since it was called photoshack, but not really getting the languge. I've done well enough for all these years, but when things change, I feel like it just goes into the too hard basket.
 
One is the way the line tool works now, and we have seen a lot of folk saying pretty much the same as you. Please post to the Feedback forum on this thread, and follow it, as that is where the Photoshop product developers have posted:
 
Second is your current document. If you deselect the path in the Paths panel and the boundary disappears, then you have an issue, as paths do not print. We haven't seen your Paths or Layers panels, but it looks to me as if you are seeing a path that is selected. It may or may not have a stroke on a layer.
 
If you are not seeing the line that you just drew, set the line stroke to Center in the Properties menu. If the line stroke is set to Inside it will not show. If it is set to Outstide, it will be 2px wide for a 1px stroke.
 
So you are unable to even select a fill color? So it is not a line or bucket problem - it is a problem with the ability to select a fill color in the first place? Can you upload the FLA? This just happens with shapes drawn with the pen tool? Weird.
 
Object Drawing Mode was turned on and if the shape was made up of more than 1 stroke segment (right?). But that wasn't how the original poster explained it - but it does make sense. You could also break all the line segments apart as well.
 
Sounds like my experience. I tried making a vector object with the Pen Tool (like I've done a billion times before in Illustrator) only to not be able to select a fill. Changing the outline color and stroke was fine. It's almost like even though it's a closed path, it/they (vector segments) needed to be closed (Union) again.
 
I think I finally figured it out. Vector lines/objects that are not closed will not fill. When you're going to finish/close the line object, it might not close. Even though the Pen Tool shows the little circle indicating you are over the end point. It appears to me this is due to a Snap selection. Try closing your vector line objects with all Snap options unselected or only **Snap to Objects** selected. This is working for me now without flaw.
 
I created a closed object with the line tool, using the snap button, but could not fill it. I resorted to a union, fill and break apart. I am using Fred Gerantabee's book on Flash CS5 and he says ithis work, but it does not in my hands.
 
Would you be able to post an example somewhere, of a closed pen drawn line that doesn't fill by using the paint bucket? I'm not able to fail to fill in the shape, so something is different about your shape.
 
Ok, so I am brand new to Illustrator as of the last two weeks, but here's my two cents. What I found to work for me and that made the most sense for what I was doing was to direct select (CTRL+A) the whole shape/stroke and make both the fill and stroke color boxes with /'s through them (clear) so it's basically invisible, then go to Object > Path > Outline Stroke, and that basically made it a shape, and then I was able to use the fill and stroke boxes like I would with a shape.
 
I am using the redaction tool in DC which I have used many times. I hit redact. Text and Images, Highlight what I want redacted and hit apply. It is redacting what I highlighted but also highlight the first letter and last of most of the other sentences on the document I did not select.
 
At the moment, I select the items I want to redact (text like 123 234 345 - that is, numbers with spaces - but the same numbers) and it does redact them, but redacts other numbers too! Should I try "123 345 456" - or something? only want to redact these numeric sequences.
 
I am having a similar problem. When I redact information on one page, black rectangles show up in the same area on the other pages of my document. I have a large image that takes up most of my document's second page. When I drag and redact it, the preview looks completely normal. However, after I apply the redaction, there is a large black rectangle on all three pages of my document.
 
I am having a similar problem. It seems that if I find and mark text for redaction it displays perfectly, but when I apply it also redacts all of the 'hidden information'. But I have not selected the hidden info for redaction.
 
My office is also having major problems with this. Now that Marsy's Law is in effect, we have to redact soooo much information from our police reports. These come from many different agencies using different software to create their PDFs. It's ridiculous that it is happening so frequently across so many different agencies' PDFs. The only thing I have found to get around it is to remove just Objects from the Remove Hidden Information section and re-run text recognition on the file. It noticeably diminshes the quality of text in the PDF. Adobe needs to fix this.
 
Hi I hae Adobe Acrobat Pro DC, and I am trying to edit things such as bring object to back or front, but the OBJECTS menu on the right side are all greyed out. I thought I have encountered this a while ago and I remember going to the preferences menu to check or uncheck something. But I cant seem to remember how I did this before. Any help is greatly appreciated. Its driving me nuts.
 
Chuck are you still available for additional questions on Mark-up Tools. I am on a PC running Windows 10 Pro. I have all mark-up tools but polygon, connected line and cloud. I tried to find a previous mark-up version that had all tools visible and follow your instructions above. All my files are coming up with these 3 tools missing. Any suggestions. Also, I have a Wacom Cintiq as a 3rd screen. that was just installed today - could that be the issue? Please advise and thank you.
 
I am unable to rotate an object such as an oval. when I enter into edit after drawing an object, the tools in right hand panel under objects are "greyed out" How do I enable these functions? Or is there another way to rotate objects? I am using the Adobe Acrobat Pro DC 2015 version.
 
I have had multiple instances where I wanted to quickly edit a PDF in Acrobat... and it has never worked properly. Most of the time, the editing tools are greyed out. For instance, I scanned in a receipt and I want to crop the image - the tool (selected from the top bar) shows a bounding box but doesn't crop. The crop function on the sidebar is completely greyed out along with all the other functions... and I don't know why. (And no, these are not password-protected / otherwise uneditable documents.)
 
Before, I wanted to quickly censor / anonymize information on a document with a few black rectangles, or add text comments beside objects. - All typical thin
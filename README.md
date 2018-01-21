# float_analyzer

The float analyzer is a simple javascript tool to analyze an image file for fabric production with the AYAB knitting machine hack.

The tool expects an image input (png file) of max 200 pixels width, max 900 pixels height, and strictly two colours, black (0,0,0) and white (255,255,255). 

The script has two functions: 
It analyzes the image file for long stretches of uninterrupted colour per row. If the stretch is longer than the allowed float_length, it marks those pixels for correction (in red). 
It then corrects the image by inserting pixels of the contrast colour into the stretch. 
For a fully corrected image both functions need to be run repeatedly. 

You can download the corrected image as you would save any image from a web page: right-click on the image and select to save the image. 

The script is embedded in an html file and needs a web server to run. To run on your local machine, use the preview feature of a text editor for web design like Brackets. (http://brackets.io/)

A number of parameters can be set in the file:

Line 13: insert your image name. The image needs to be located in the same folder as your script file. 

Line 37: `float_length`, `float_offet` and `num_of_interactions`

`float_length` is the longest float that will be allowed. 
`float_offset` is the length of floats allowed before a correction will be applied. 
`num_of_iterations` is how often the script cycles through rounds of analysis and correction. 


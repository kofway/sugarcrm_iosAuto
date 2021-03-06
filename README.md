Repo for ios automation connector


This project, currently named trio, is dedicated to bring us automation for different mobile platforms. Right now it only supports iOS automation using the instruments.app provided by apple. The test cases themselves use javascript to perform UI interactions. As a result, we need to familiar outselves with the syntax and format of the test cases. 

First thing, we should clone the sugarcrm/PhoneVooDoo repository and check the files under the folder Trio. The powerpoint document is a good starting point to gain some knowledge towards what this piece of code does. 

The text.xml is the "test file" that testers will write. The output.js is the converted javascript tests mentioned above. Currently trio only converts the xml file to javascript. In the future we should implement it in a way such that it will also push the converted test to instruments and have it run the converted test(refer to [1]). 

There are some useful links provided in ref#2 to help us understand the whole iOS automation process. Also there's been enhancements done by apple to make our lives easier[3]. We will also want to be able to run trio through command line as well in order to make it friendly for CI automation process. Trio uses documentbuilder for xml parsing, so some knowledge regarding the w3c dom libraries are recommended[4].


[1]Right now we do not support pushing the converted javascript directly from the java class since we are using iOS 4.x simulators and a older version of xcode. However, this is now doable by using command line on iOS 5 beta4:
http://lemonjar.com/blog/?p=69
http://dev-ios.blogspot.com/2011/07/starting-uiautomation-via-command-line.html

[2]Some useful links regarding the automation process:
http://alexvollmer.com/posts/2010/07/03/working-with-uiautomation/
http://cocoamanifest.net/articles/2011/05/uiautomation-an-introduction.html
http://developer.apple.com/library/ios/#DOCUMENTATION/UserExperience/Conceptual/MobileHIG/UIElementGuidelines/UIElementGuidelines.html
http://www.codeproject.com/KB/iPhone/UI_Automation_Testing.aspx

[3]Some interesting information regarding the changes to iOS 5 automation:
http://cocoamanifest.net/articles/2011/11/changes-to-ui-automation-in-ios-5.html

[4]DOM reference:
http://www.w3schools.com/dom/dom_document.asp
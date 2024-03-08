# UiPath Automation Cloud Use Case

## Use Case
First line of defense from ticket scalpers for Taylor Swift concert tickets.

Scenario: 
- Only fans with a special code are allowed to enter the website to purchase her tour tickets
  
UiPath Workflow: 
- A user needs to fill out a form that includes the special code and click the “Next” button to access the website
- When the correct special code “SwiftiesForever” is entered, users will be guided to the website (https://www.taylorswift.com/tour/)
- When the wrong special code is entered, users will receive an error message and unable to access the website
  
Logic: 
- UiPath will check if the code is correct to allow fans into the site to view tour dates and buy tickets

## App Demo/Testing
![](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/blob/main/CorrectCode_Testing.gif) <br>
The GIF above shows the scenario when the correct secret code was used. By clicking on the “Next” button, it guided the user to the tour page. By clicking on the “Back” button, it guided user to the main page. 

The next GIF above shows the scenario when the wrong secret code was used. The error message popped up. The test was also done on the mandatory email field, where the field becomes red and mentions that it’s required to fill in when there’s none.

#### Error Screenshots
![error1](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/18ea9ac1-414f-4266-a2c9-236e2257b114) <br>
![error2](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/17296c9d-f1ef-4193-a1e5-dab9293a966f)


## Constructing App
Firstly, a new app was created in the UiPath Automation Cloud and FormA template was used. 
![Picture 1](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/a5ca3d7e-4d77-4c35-ae70-6a0f6977ffee) <br>
Screenshot 1 <br>
This form was then adapted to collect information of the person accessing the website. 


![Picture 2](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/2c09387b-fe05-4528-a353-4ccc33f16edb)<br>
Screenshot 2 <br>
All unnecessary fields were deleted and the header, fields, button colors were changed. 


![Picture 3](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/afc50e2c-2ebd-4d49-a5a0-3e3d0be7dc07) <br>
Screenshot 3 <br>
![Picture 4](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/51e123e3-04e5-4003-913b-9105e41a4009) <br>
Screenshot 4 <br>
Both email address and secret code fields were set to be mandatory by entering “=true” in the “Required” field.


![Picture 5](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/33c7b17e-ee88-4f67-ab38-30283f02950a) <br>
Screenshot 5 <br>
As the Secret Code needs to be validated when someone clicks on the “Next” button, an app variable was created and dragged to the value binding field. 


![Picture 6](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/9812f37a-2748-40f0-bb94-63d09323e0e0) <br>
Screenshot 6 <br>
A condition was added to the “Next” button to validate the code by clicking on “Edit Rule” in the “Events” tab. 


![Picture 7](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/baca5aef-9484-4407-b595-be773b75bfdd) <br>
Screenshot 7 <br>
If-Else condition was added. <br>
- If: “SecretCode” app variable was dragged here, equal operator used, and secret code “Swifties Forever” was set <br>
- Then: The App will open the ticket purchase URL on a new tab <br>
- Else: An error message will show for 5 seconds at the top <br>

![Picture 8](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/9074c4aa-7401-44d5-9829-cee8f27a43f4) <br>
Screenshot 8 <br>
A rule was created for the “Back” button as well.

![Picture 9](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/fd9126e9-c406-421a-a39c-bee07b7ca032) <br>
Screenshot 9 <br>
This button will lead users to the main webpage on the same tab. 

![Picture 10](https://github.com/Kfkyyian1/uipath_automation_cloud_concertickets/assets/146427900/f8b25e46-9ea3-4dfb-ba84-ea0a813c9e64) <br>
Screenshot 10 <br>
As the form is complete and conditions are set, it can be observed that there’s a lightning icon beside the buttons indicating that there’s a condition. 
















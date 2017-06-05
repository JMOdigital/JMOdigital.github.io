---
layout: post
cover: 'assets/images/polymers.jpg'
title:  Building a health calculator with Google Polymers
date:   2016-06-22 10:18:00
tags: coding
subclass: 'post tag-coding'
categories: martin
navigation: True
logo: 'assets/images/ghost.png'
author: martin
disqus: False
---


> Adapted from the *Coding 101* workshop delivered at the 2015 Future Health Leaders Conference in Sydney. 
> Thanks to Kevin Gleason (@kevinagleason) for his Polymer ToDo tutorial, which provided some inspiration. Some of the app layouts have been drawn from his code under the provisions of the MIT license. 

### Aim
Simple software applications have the power to transform the *user-experience* of healthcare for both clinicians and patients. Thanks to increasingly intuitive development frameworks, web apps for tracking your own health data, scheduling appointments, task allocation and decision support are now easier to build than ever before. This will be a hands-on tutorial showing you how to write a short piece of code for a healthcare application. We will use Javascript and Google Polymers to guide you through the process of building a simple calculator app to generate, for example, a BMI, or a Wells Score, or an osteoporosis risk. 


### Prerequisites
The tutorial is designed for those with ZERO programming experience. 

### Downloads

##### Essential
- A text editor for writing code e.g. [SublimeText](http://www.sublimetext.com/download)

- Software to run a local server to test out your code e.g. [Python](https://www.python.org/downloads/)
*(NB. versions 2 and 3 acceptable, available for Mac/Windows/Linux)*


##### Optional but helpful
- A package manager to download dependencies [Node.js and Node Package Manager](https://nodejs.org/en/)
- Version control for tracking your changes and uploading to the internet: [Git](http://git-scm.com)
- A clever piece of software for updating dependencies: [Bower](http://bower.io)

___

### Finished product
Below is a screenshot of the finished calculator app that you will develop! 

![Finished calculator app]({{site.baseurl}}assets/images/calculator.png)

___

### Setup

##### Step 1
Ensure you have downloaded Python (version 2 or 3) and a text editor for editing the code. See above for details. 

Download the [template app](https://github.com/martinsen/FHLtute)

This includes all the views and formatting to make your life easier, so you can just focus on the logic. 

##### Step 2
Open the terminal in your computer.

Navigate into the FHL tutorial folder.
```cd FHLtutorial
```

##### Step 3
Run a local server to test your app. 

```python
For Python 2:
python -m SimpleHTTPServer   

For Python 3: 
 Python 3 python -m http.server
 ```
 
##### Step 4
Run a local server to test your app. 

Open the browser to: [http://localhost:8000](http://localhost:8000)

___

### Input

The file you will mainly be dealing with is the calculator.html file. 

Fire up your text editor (SublimeText) and open *calculator.html*

Scroll down halfway to the *Questionnaire input* section, where we see 3 different kinds of inputs: 

- Text or numerical input (paper-input) for which the range or number of characters can be specified.
- Checkbox input (paper-checkbox)
- Multiple choice input (paper-radio-group)

```html
<!--Questionnaire input -->
<paper-material id="todoEntry" elevation="2">
	<paper-input id="tName" char-counter label="First Name / ID" maxlength="20" 
	error="maximum characters exceeded" style="width:65%"> ></paper-input>
	
	<paper-input id="tAge" label="Age" pattern="[0-9]{2,3}" auto-validate 
	error-message="Invalid age!"> ></paper-input>	
	
	<paper-input id="tWeight" label="Weight in kilograms" type="number" min="20" 
	max="250" auto-validate error-message="Invalid weight!"></paper-input>
	
	<paper-input id="tHeight" label="Height in centimetres" type="number" min="50" 
	max="250" auto-validate error-message="Invalid height!"></paper-input>
					
 	<paper-checkbox id="checkboxInput"><b>Example checkbox input</b></paper-checkbox>
					
	<h4 class="question-title">Example MCQ input</h4>
	<paper-radio-group id = "MCQ">
		<paper-radio-button name="1" value="1">Small</paper-radio-button>
		 <paper-radio-button name="2" value= "2">Medium</paper-radio-button>
		 <paper-radio-button name="3" value= "3">Large</paper-radio-button>
	</paper-radio-group>

<paper-fab icon="icons:arrow-forward" on-tap="calculate"></paper-fab>
</paper-material>
```
___
### Output/Calculation

Here is the real logic, where we use our inputs from section 1 to calculate a score. Below is a single javascript function called *calculate* which defines *local variables* corresponding to the inputs from section 1. The function then checks whether the inputs have any data and, if so, assigns these data to the local variables. Finally, the function calculates a score, in this case BMI, using the local variables and some simple Javascript maths (see next page for the syntax of some common maths functions). Note that we are not using all our variables in this example - you can customise your inputs to get just the right information you need for your calculation. The endgame is to assign a new value for *this.score*, which is a *property* that we have defined in the code just above. 

```javascript

calculate: function(e) {
    	this.score = 0;

    	var weight;
    	var age;
    	var height;
    	var check;
    	var MCQ;
	
	    if(this.$.tWeight) {
	    	weight = parseInt(this.$.tWeight.value) || 0;
	    }
	    if (this.$.tAge){
  			age = parseInt(this.$.tAge.value) || 0;
  		}
  		if (this.$.MCQ.selected){
  			MCQ = parseInt(this.$.MCQ.selected)||0;
  		}
  		if (this.$.tHeight){
  			height = parseInt(this.$.tHeight.value)||0;
  		}
  		switch (this.$.checkboxInput.checked){
  			case true:
  			    check = 2
  			    break;
  			case false:
  			    check = 0
  			    break;
  		}

	    var BMI = (weight/(Math.pow((height/100),2)));

	    this.score = +(BMI.toFixed(2));
	    this.unshift('done',{value:this.score, name:this.$.tName.value});
    },
    
```

##### Javascript maths reference
```javascript
Math.abs(a)     // the absolute value of a
Math.acos(a)    // arc cosine of a
Math.asin(a)    // arc sine of a
Math.atan(a)    // arc tangent of a
Math.atan2(a,b) // arc tangent of a/b
Math.ceil(a)    // integer closest to a and not less than a
Math.cos(a)     // cosine of a
Math.exp(a)     // exponent of a (Math.E to the power a)
Math.floor(a)   // integer closest to a, not greater than a
Math.log(a)     // log of a base e
Math.max(a,b)   // the maximum of a and b
Math.min(a,b)   // the minimum of a and b
Math.pow(a,b)   // a to the power b
Math.random()   // pseudorandom number 0 to 1 (see examples)
Math.round(a)   // integer closest to a (see rounding examples)
Math.sin(a)     // sine of a
Math.sqrt(a)    // square root of a
Math.tan(a)     // tangent of a
```

___

###Score Dial

Now we are going to hook up the score to a score dial like this: 
![Score dial]({{site.baseurl}}assets/images/dial.png)


In the template section: 

```
<!--Score feedback with dial -->
<paper-material>
<paper-item elevation="4"> <h2>Total score: <span>{{score}}</span></h2></paper-item>
		<google-chart
			type='gauge'
			id = 'gaugeChart'
			options='{
					"redFrom": 35,
					"redTo": 50,
					 "yellowFrom": 25,
					 "yellowTo": 35,
					 "max":50,
					 "minorTicks": 5}'
					data='[["Label", "Value"],
					["Score", 0]]'>
		</google-chart>
</paper-material>
```

In the Javascript *calculate* function: 

```javascript
...in calculate: function(e) { 
    	    ...
	    this.$.gaugeChart.data = [["Label", "Value"],["", (this.score)]];
	    ...
```

___

###Recommendations
Finally, we link up the score to relevant text recommendations.

In the template section: 
```
<!--Recommendations for further action -->
<paper-material>
	<paper-item><h2>Recommendations</h2></paper-item>
	<paper-item id="recommendText">Text goes here</paper-item>
	<google-hangout-button id="callButton"></google-hangout-button>
</paper-material>
```

In the Javascript section, define a new function called *stratify*. This function takes the score and uses the Javascript *switch* function to do different things depending on which range the score falls into. Here we have three case scenarios. Each case sets the recommendation text to a different output. It also adjusts the value of a boolean parameter *callDoc* which we use as a switch to make a particular button (a google hangout button defined above) disappear or appear. Imagine this as a tele-medecine link - if your score is in a dangerous range, a google-hangout button appears for you to reach out: 

```javascript
stratify: function(e){
   		var x = this.score;
   		switch(true){
   			case (x<=17):
   				callDoc=false;
   				this.$.recommendText.innerHTML = "Your BMI is too low";
   				break;
   			case (x > 17 && x < 25):
   				callDoc=false;
   				this.$.recommendText.innerHTML = "BMI within range";
   				break;
   			case (x >=25):
   				callDoc=true;
   				this.$.recommendText.innerHTML = "BMI too high.";
   				break;
   		}
   		this.$.callButton.hidden = !callDoc;
   	},
    ready: function(e){
	}
```
___

###Conclusion
Congratulations. Now it's time to play around with your new app. You can build in more features like charts, maps and tables using the ever-growing catalogue of Polymer elements. Read more about these elements [here](https://elements.polymer-project.org/). You can even design your own reusable elements to incorporate into further web development projects - this is the future of modular web development! 



# CSS Selector CheatSheet

1. **Absolute CSS Selectors**

```xml

In this selector (>) sign is used to reach til element.
Example : form>div>div>span>form>div>input
```

2. **Relative CSS Selectors**

```xml

You should use white space between tags to locate the element. Use “.” for class and “#” for id.
Example : form .form-group #user-message
	
```

3. **Find Element By ID**

```xml

Syntax : #idValue
Example : #first-name
		
```

4. **Find Element By Class**

```xml

Syntax : .classValue
Example : .txtInput
		
```

5. **Find Element By Multiple Classes**

```xml

Syntax : .class1Value.class2Value
Example : .form-input.txtInput
		
```
	
6. **Find Element By Class & Attribute**

```xml

Syntax : .className[attribute='attributeValue']
Example : .txtInput[type='text']
		
```

7. **Find Child Elements  (Search Immediate Child)**

```xml

Syntax : ParentElement>ChildElement
Example : div[id='first-name']>input
		
```

8. **Find Descendent Elements (Search All Child Elements)**

```xml

Syntax : ParentElement ChildElement
Example : div[id='first-name'] input
		
```

9. **nth-child(n) method in CSS Selector**

```xml

Syntax : ParentElement ChildElement:nth-child(n)
Note : Index (n) starts from 1
Example : table>tbody>tr:nth-child(3)
		
```

10. **nth-of-type(n) method in CSS Selector**

```xml

Syntax : ParentElement ChildElement:nth-of-type(n)
Example : form[id'form1']>label:nth-of-type(3)
		
```

11. **Finding First Child Element**
```xml

Syntax : ParentElement ChildElement:first-child
Example : table>tbody>tr:first-child
Example : table>tbody>tr:first-child>td:first-child
		
```	

12. **Finding last Child Element**
```xml

Syntax : ParentElement ChildElement:last-child
Example : table>tr:last-child
Example : table>tbody>tr:last-child>td:last-child
		
```

13. **Finding Element by Prefix (Elements starts with...)**
```xml

Syntax : [attribute^='attributePrefixValue']
Example : [id^='last-name']

Syntax : tagName[attribute^='attributePrefixValue']
Example : input[id^='first-name']	
		
```

14. **Finding Element by Suffix  (Elements ends with...)**
```xml

Syntax : [attribute$='attributeSufixValue']
Example : [id$='last-name']

Syntax : tagName[attribute$='attributeSufixValue']
Example : input[id$='first-name']
		
```

15. **Finding Element with partial Attribute Value  (This is like contains() method)**
```xml

Syntax : [attribute*='partialAttributeValue']
Example : [id*='name']

Syntax : tagName[attribute*='partialAttributeValue']
Example : input[id*='first']
		
```

16. **Finding Immediate Sibling (Searches next sibling element)**
```xml

Syntax : cssSelectors + immediateSiblingElement
Example : label[id='first-name'] + input
Example : label[id='first-name'] + input + span
Example : label[id='first-name'] + input + span + label
		
```

17. **Finding Following Sibling**
```xml

Syntax : cssSelectors ~ followingSiblingElement
Example : label[id='first-name'] ~ input
Example : label[id='first-name'] ~ input ~ span
Example : label[id='first-name'] ~ input ~ span ~ label
Example : label[id='first-name'] ~ input:nth-child(1)
Example : label[id='first-name'] ~ input:nth-of-type(3)
		
```

18. **Finding Element by ignoring case sesitivity**
```xml

Syntax : [attribute='attributeValue' i]
Example : [id='first-name' i]

Syntax : tagName[attribute='attributeValue' i]
Example : label[id='first-name' i]
		
```	


# Search It

1. How to use and, or operator in css selector...?

2. How to index same element and not child element...?




# XPath CheatSheet

# Absoulte XPath

```xml

It contains the complete path from the Root Element to the desire element.
Example : /html/body/div[2]/div[1]/div/header/div/div/div/div/div/div/div[2]

```
	
# Relative XPath

```xml

It starts from the middle of HTML DOM structure. It starts with double forward slash (//). It can search elements anywhere on the webpage, means no need to write a long xpath and you can start from the middle of HTML DOM structure.
Example : //a[@href='/ask-doubt']

```


# Locating Elements with Multiple Attributes

```xml

Syntax: //*[attribute1=’value1’][attribute2=’value2’]…[attributeN=’valueN’]
Example : //*[@type='text'][@name='firstName']

Syntax: //tagName[attribute1=’value1’][attribute2=’value2’]…[attributeN=’valueN’]
Example : //input[@type='text'][@name='firstName']

Syntax: //*[attribute1=’value1’ and attribute2=’value2]
Example : //*[@type='text' and @name='firstName']

Syntax: //tagName[attribute1=’value1’ and attribute2=’value2]
Example ://input[@type='text' and @name='firstName']	

```

# XPath using operator	

1. **Equal (=) Operator**	

```xml

Syntax: //XPath with Attribute/conditon/function = value
Example : //td[text()=999]	

```

2. **Not Equal (!=) Operator**	

```xml		

Syntax: //XPath with Attribute/conditon/function != value
Example : //td[text()!=999]

```

3. **Less than (<) Operator**	

```xml		

Syntax: //XPath with Attribute/conditon/function < value
Example : //td[text()<999]

```

4. **Greater Than (>) Operator**	

```xml		

Syntax: //XPath with Attribute/conditon/function > value
Example : //td[text()>999]

```

5. **Less Than or Equal (<=) Operator**	

```xml		

Syntax: //XPath with Attribute/conditon/function <= value
Example : //td[text()<=999]

```

6. **Greater Than or Equal (>=) Operator**	

```xml		

Syntax: //XPath with Attribute/conditon/function >= value
Example : //td[text()>=999]

```

7. **OR (or) Operator**		

```xml		

Syntax: //XPath with Attribute/conditon/function or value
Example : //input[@id='phone' or @type='text']

```

8. **And (and) Operator**	

```xml		

Syntax: //XPath1 [with Attribute1/conditon1/function1 and value1]
Example : //input[@id='phone' and @type='text']

Syntax: //XPath1 [with Attribute1/conditon1/function1 and value] [with Attribute2/conditon2/function2 and value2]		
Example : //input[@id='phone'][@type='text']

```

# XPath Methods

1. **last()**

```xml
Syntax: //*[last()]
Example: //*[last()]

Syntax: //tagName[last()]
Example: //input[last()]

Syntax: //*[Xpath][last()]
Example: //*[@name='firstName'][last()]

Syntax: //tagName[Xpath][last()]
Example: //input[@name='firstName'][last()]

Syntax: //*[position()=last()]
Example: //*[position()=last()]

Syntax: //tagName[position()=last()]
Example: //input[position()=last()]

```

2. **text()**

```xml

Syntax: //*[text()='Text to search']
Example: //*[text()='firstName']

Syntax: //tagName[text()='Text to search']
Example: //input[text()='firstName']

```

3. **contains()**

```xml

Syntax: //*[contains(text(),'Text to search')]
Example: //*[contains(text(),'firstName')]

Syntax: //tagName[contains(text(),'Text to search')]
Example: //input[contains(text(),'abhijit']

Syntax: //*[contains(.,'Text to search')]
Example: //*[contains(.,'firstName')]

Syntax: //tagName[contains(.,'Text to search')]
Example: //input[contains(.,'abhijit')]

Syntax: //*[contains(@attribute,'Text to search')]
Example: //*[contains(@text,'abhijit')]

Syntax: //tagName[contains(@attribute,'Text to search')]
Example: //input[contains(@text,'abhijit')]

```

4. **starts-with()**

```xml

Syntax: //*[starts-with(text(),'Text to search')]
Example: //*[starts-with(text(),'abhijit'))]

Syntax: //tagName[starts-with(text(),'Text to search')]
Example: //input[starts-with(text(),'abhi')]

Syntax: //*[starts-with(@attribute,'Text to search')]
Example: //*[starts-with(@name,'abhijit']

Syntax: //tagName[starts-with(@attribute,'Text to search')]
Example: //input[starts-with(@attribute,'abhi')]


```

5. **ends-with()**

```xml

Syntax: //*[ends-with(text(),'Text to search')]
Example: //*[ends-with(text(),'jit'))]

Syntax: //tagName[ends-with(text(),'Text to search')]
Example: //input[ends-with(text(),'jit')]

Syntax: //*[ends-with(@attribute,'Text to search')]
Example: //*[ends-with(@name,'jit']

Syntax: //tagName[ends-with(@attribute,'Text to search')]
Example: //input[ends-with(@attribute,'jit')]


```

6. **position()**

```xml

Syntax: //*[text()='Text to search']/tr/td[5]
Example: //*[text()='userName']/tr/td[5]

Syntax: //tagName[text()='Text to search']/tr/td[5]
Example: //input[text()='userName']/tr/td[5]

Syntax: //*[text()='Text to search']/tr/td[position()=5]
Example: //*[text()='userName']/tr/td[position()=5]

Syntax: //tagName[text()='Text to search']/tr/td[position()=5]
Example: //input[text()='userName']/tr/td[position()=5]

Syntax: //*[text()='Text to search']/tr/td[last()]
Example: //*[text()='userName']/tr/td[last()]

Syntax: //tagName[text()='Text to search']/tr/td[last()]
Example: //input[text()='userName']/tr/td[last()]

Syntax: //*[text()='Text to search']/tr/td[last()-1]
Example: //*[text()='userName']/tr/td[last()-1]

Syntax: //tagName[text()='Text to search']/tr/td[last()-1]
Example: //input[text()='userName']/tr/td[last()-1]

Syntax: //*[text()='Text to search']/tr/td[last()-2]
Example: //*[text()='userNameh']/tr/td[last()-2]

Syntax: //tagName[text()='Text to search']/tr/td[last()-2]
Example: //input[text()='userName']/tr/td[last()-2]

Syntax: //*[text()='Text to search']/tr[position()>1]/td[5]
Example: //*[text()='userName']/tr[position()>1]/td[5]

Syntax: //tagName[text()='Text to search']/tr[position()>1]/td[5]
Example: //input[text()='userName']/tr[position()>1]/td[5]

Syntax: //*[text()='Text to search']/tr[position()<3]/td[5]
Example: //*[text()='userName']/tr[position()<3]/td[5]

Syntax: //tagName[text()='Text to search']/tr[position()<3]/td[5]
Example: //input[text()='userName']/tr[position()<3]/td[5]

Syntax: //*[text()='Text to search']/tr[position()>=1]/td[5]
Example: //*[text()='userName']/tr[position()>=1]/td[5]

Syntax: //tagName[text()='Text to search']/tr[position()>=1]/td[5]
Example: //input[text()='userName']/tr[position()>=1]/td[5]

Syntax: //*[text()='Text to search']/tr[position()<=3]/td[5]
Example: //*[text()='userName']/tr[position()<=3]/td[5]

Syntax: //tagName[text()='Text to search']/tr[position()<=3]/td[5]
Example: //input[text()='userName']/tr[position()<=3]/td[5]

```


# Normalize - space XPath

```xml

Syntax: //*[normalize-space(text()),'Text to search']
Example : //*[normalize-space(text()),'abhijit biradar']

Syntax: //label[normalize-space(text()),'Text to search']
Example : //label[normalize-space(text()),'abhijit biradar']

Syntax: //*[normalize-space(@id)='Text to search']
Example : //*[normalize-space(@id)='abhijit biradar']

Syntax: //label[normalize-space(@id)='Text to search']
Example : //label[normalize-space(@id)='abhijit biradar']

```
	
# Group Index XPath

```xml

Syntax: (//*[text()='Text to search'])[3]
Example : (//*[text()='biradar'])[3]

Syntax: (//tagName[text()='Text to search'])[3]
Example : (//input[text()='biradar'])[3]

```

# XPath Axes	

1. **Parent Element in XPath**

```xml

Syntax: //XPath/Parent::*
Example : //input[@name='firstName']/parent::*

Syntax: //XPath/Parent::tagName
Example : //input[@name='firstName']/parent::div

Syntax: //XPath/..
Example : //input[@name='firstName']/..

Syntax: //Parent[XPath]
Example : div[//input[@name='firstName']]

Syntax: //XPath/parent::XPath
Example : //input[@name='firstName']/parent::table[@id='customer']

```

2. **Child Element in XPath**

```xml

Syntax: //XPath/child::*
Example : //input[@name='firstName']/child::*

Syntax: //XPath/child::tagName
Example : //input[@name='firstName']/child::div

Syntax: //XPath/tagName
Example : //input[@name='firstName']/div

Syntax: //XPath/child::XPath
Example : //input[@name='firstName']/child::table[@id='customer']

```

3. **Ancestor Element in XPath (Ancestor = Parent Upto Root Element)**

```xml

Syntax: //XPath/ancestor::*
Example : //input[@name='firstName']/ancestor::*

Syntax: //XPath/ancestor::tagName
Example : //input[@name='firstName']/ancestor::div

Syntax: //XPath1/ancestor::XPath2
Example : //input[@name='firstName']/ancestor::table[@id='customer']

```

4. **Descendent Element in XPath (descendant= Children and Grand Children)**

```xml

Syntax: //XPath/descendant::*
Example : //input[@name='firstName']/descendant::*

Syntax: //XPath/descendant::tagName
Example : //input[@name='firstName']/descendant::div[3]

Syntax: //XPath/descendant::XPath
Example : //input[@name='firstName']/descendant::table[@id='customer']

```

5. **Following Element in XPath (Following= All elements following or after that element)**

```xml

Syntax: //XPath/following::*
Example : //input[@name='firstName']/following::*

Syntax: //XPath/following::tagName
Example : //input[@name='firstName']/following::div[3]

Syntax: //XPath/following::XPath
Example : //input[@name='firstName']/following::div[3]/tr[3]/td[1]

```

6. **Following-sibling Element in XPath (Following-sibling= All sibling of reference element after that element)**

```xml

Syntax: //XPath/following-sibling::*
Example : //input[@name='firstName']/following-sibling::*

Syntax: //XPath/following-sibling::tagName
Example : //input[@name='firstName']/following-sibling::div[3]

Syntax: //XPath/following-sibling::XPath
Example : //input[@name='firstName']/following-sibling::div[3]/tr[3]/td[1]

```

7. **Preceding Element in XPath (Preceding= All elements before that element)**

```xml

Syntax: //XPath/preceding::*
Example : //input[@name='firstName']/preceding::*

Syntax: //XPath/preceding::tagName
Example : //input[@name='firstName']/preceding::div[3]

Syntax: //XPath/preceding::XPath
Example : //input[@name='firstName']/preceding::div[3]/tr[3]/td[1]	

```

8. **Preceding-sibling Element in XPath (Preceding-sibling= All sibling of reference element before that element)**

```xml

Syntax: //XPath/preceding-sibling::*
Example : //input[@name='firstName']/preceding-sibling::*

Syntax: //XPath/preceding-sibling::tagName
Example : //input[@name='firstName']/preceding-sibling::div[3]

Syntax: //XPath/preceding-sibling::XPath
Example : //input[@name='firstName']/preceding-sibling::div[3]/tr[3]/td[1]

```

9. **Ancestor-or-self Element in XPath** 

```xml

Syntax: //XPath/ancestor-or-self::*
Example : //input[@name='firstName']/ancestor-or-self::*

Syntax: //XPath/ancestor-or-self::tagName
Example : //input[@name='firstName']/ancestor-or-self::div

Syntax: //XPath1/ancestor-or-self::XPath2
Example : //input[@name='firstName']/ancestor-or-self::table[@id='customer']

```

10. **Descendent-or-self Element in XPath**  

```xml

Syntax: //XPath/descendent-or-self::*
Example : //input[@name='firstName']/descendent-or-self::*

Syntax: //XPath/descendent-or-self::tagName
Example : //input[@name='firstName']/descendent-or-self::div[3]

Syntax: //XPath/descendent-or-self::XPath
Example : //input[@name='firstName']/descendent-or-self::table[@id='customer']

```

11. **self**

```xml

Syntax: //XPath/self::*
Example : //input[@name='firstName']/self::*

Syntax: //XPath/self::tagName
Example : //input[@name='firstName']/self::div[3]

Syntax: //XPath/self::XPath
Example : //input[@name='firstName']/self::div[3]/tr[3]/td[1]

```


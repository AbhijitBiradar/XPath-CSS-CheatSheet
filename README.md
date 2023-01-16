# CSS CheatSheet

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
Syntax : tagName[attribute^='attributePrefixValue']
Example : [id^='last-name']
Example : input[id^='first-name']	
		
```

14. **Finding Element by Suffix  (Elements ends with...)**
```xml

Syntax : [attribute$='attributeSufixValue']
Syntax : tagName[attribute$='attributeSufixValue']
Example : [id$='last-name']
Example : input[id$='first-name']
		
```

15. **Finding Element with partial Attribute Value  (This is like contains() method)**
```xml

Syntax : [attribute*='partialAttributeValue']
Syntax : tagName[attribute*='partialAttributeValue']
Example : [id*='name']
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
Syntax : tagName[attribute='attributeValue' i]
Example : [id='first-name' i]
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
Syntax: //tagName[last()]
Example: //input[last()]

Syntax: //*[Xpath][last()]
Example: //input[@name='firstName'][last()]

Syntax: //Xpath[position()=last()]
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

Syntax: //*[contains(.,'Text to search')]
Example: //*[contains(.,'firstName')]

Syntax: //tagName[contains(text(),'Text to search')]
Example: //input[contains(text(),'abhijit']

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

Syntax: //*[text()='Text to search']/tr/td[5]Example: 
Example: 

Syntax: //tagName[text()='Text to search']/tr/td[5]
Example: 

Syntax: //*[text()='Text to search']/tr/td[position()=5]
Example: 

Syntax: //tagName[text()='Text to search']/tr/td[position()=5]
Example: 

Syntax: //*[text()='Text to search']/tr/td[last()]
Example: 

Syntax: //tagName[text()='Text to search']/tr/td[last()]
Example: 

Syntax: //*[text()='Text to search']/tr/td[last()-1]
Example: 

Syntax: //tagName[text()='Text to search']/tr/td[last()-1]
Example: 

Syntax: //*[text()='Text to search']/tr/td[last()-2]
Example: 

Syntax: //tagName[text()='Text to search']/tr/td[last()-2]
Example: 

Syntax: //*[text()='Text to search']/tr[position()>1]/td[5]
Example: 

Syntax: //tagName[text()='Text to search']/tr[position()>1]/td[5]
Example: 

Syntax: //*[text()='Text to search']/tr[position()<3]/td[5]
Example: 

Syntax: //tagName[text()='Text to search']/tr[position()<3]/td[5]
Example: 

Syntax: //*[text()='Text to search']/tr[position()>=1]/td[5]
Example: 

Syntax: //tagName[text()='Text to search']/tr[position()>=1]/td[5]
Example: 

Syntax: //*[text()='Text to search']/tr[position()<=3]/td[5]
Example: 

Syntax: //tagName[text()='Text to search']/tr[position()<=3]/td[5]
Example: 

```
























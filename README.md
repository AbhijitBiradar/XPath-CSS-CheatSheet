# CSS CheatSheet

Absolute CSS Selectors
	In this selector (>) sign is used to reach til element.
	Example : form>div>div>span>form>div>input


Relative CSS Selectors
	You should use white space between tags to locate the element. Use “.” for class and “#” for id.
	Example : form .form-group #user-message
	
	
Find Element By ID	
	Syntax : #idValue
	Example : #first-name


Find Element By Class
	Syntax : .classValue
	Example : .txtInput


Find Element By Multiple Classes
	Syntax : .class1Value.class2Value
	Example : .form-input.txtInput
	
	
Find Element By Class & Attribute
	Syntax : .className[attribute='attributeValue']
	Example : .txtInput[type='text']


Find Child Elements  (Search Immediate Child)
	Syntax : ParentElement>ChildElement
	Example : div[id='first-name']>input


Find Descendent Elements (Search All Child Elements)
	Syntax : ParentElement ChildElement
	Example : div[id='first-name'] input


nth-child(n) method in CSS Selector   
	Syntax : ParentElement ChildElement:nth-child(n)
	Note : Index (n) starts from 1
	Example : table>tbody>tr:nth-child(3)


nth-of-type(n) method in CSS Selector
	Syntax : ParentElement ChildElement:nth-of-type(n)
	Example : form[id'form1']>label:nth-of-type(3)


Finding First Child Element
	Syntax : ParentElement ChildElement:first-child
	Example : table>tbody>tr:first-child
	Example : table>tbody>tr:first-child>td:first-child


Finding last Child Element
	Syntax : ParentElement ChildElement:last-child
	Example : table>tr:last-child
	Example : table>tbody>tr:last-child>td:last-child


Finding Element by Prefix (Elements starts with...)
	Syntax : [attribute^='attributePrefixValue']
	Syntax : tagName[attribute^='attributePrefixValue']
	Example : [id^='last-name']
	Example : input[id^='first-name']	


Finding Element by Suffix  (Elements ends with...)
	Syntax : [attribute$='attributeSufixValue']
	Syntax : tagName[attribute$='attributeSufixValue']
	Example : [id$='last-name']
	Example : input[id$='first-name']


Finding Element with partial Attribute Value  (This is like contains() method)
	Syntax : [attribute*='partialAttributeValue']
	Syntax : tagName[attribute*='partialAttributeValue']
	Example : [id*='name']
	Example : input[id*='first']


Finding Immediate Sibling (Searches next sibling element)
	Syntax : cssSelectors + immediateSiblingElement
	Example : label[id='first-name'] + input
	Example : label[id='first-name'] + input + span
	Example : label[id='first-name'] + input + span + label


Finding Following Sibling
	Syntax : cssSelectors ~ followingSiblingElement
	Example : label[id='first-name'] ~ input
	Example : label[id='first-name'] ~ input ~ span
	Example : label[id='first-name'] ~ input ~ span ~ label
	Example : label[id='first-name'] ~ input:nth-child(1)
	Example : label[id='first-name'] ~ input:nth-of-type(3)


Finding Element by ignoring case sesitivity
	Syntax : [attribute='attributeValue' i]
	Syntax : tagName[attribute='attributeValue' i]
	Example : [id='first-name' i]
	Example : label[id='first-name' i]
	

How to use and, or operator in css selector...?

hot to index same element and not child element...?

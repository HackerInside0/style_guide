<center>
<h1> C++ coding style guide </h1>
<h2> by qub1750ul </h2>
</center>

[![GitHub tag](https://img.shields.io/github/tag/qub1750ul/style-guide.svg?label=Release)]()

### Index ###

- [Code blocks nesting and identation](#code-blocks-nesting-and-identation)
- [One line conditional structures](#one-line-conditional-structures)
- [Functions](#functions)

## Code block's nesting and identation ##

~~~c++
if( condition )
	{
		// then code
	}
	else
	{
		// else code

		while( wCondition )
			{
				// loop code
			}
	}
~~~

#### key characteristics ####

&nbsp; **Identation character:** tab  
&nbsp; **Identation dimension:** 1 tab ( 2 spaces ) for level  

#### other notes ####

-   Every code block included in curly braces begins on the newline that follows the statament that introduces it.  
-   The **curly braces** have one level of **indentation** form the opening statement.  
<br>
-   The code begins on the newline that follows the opening curly brace.  
-   The **code** has one level of **indentation** from the curly braces, two levels from the opening statement.  
<br>
-   The arguments between simple braces are **always** at a distance of one space from the braces itself.

<br>

## One line conditional structures ##
### Short style ###
~~~c++
if( condition ) instruction;
~~~
~~~c++
for( initializer; condition; modifier ) instruction;
~~~
~~~c++
do instruction while( condition );
~~~
### Long style ###
~~~c++
if( condition )
	this_is_a_very_long_instruction;
~~~
~~~c++
for( initializer; condition; modifier )
	really_very_very_very_long_one-line_instruction;
~~~
~~~c++
do another_very_long_instruction
	while( condition );
~~~

<br>

## Functions ##
~~~c++
type myFunction( type argument0, type argument1 )
	{
		// whatever you want
	}
~~~

Function declaration and definition style follows the rules early adopted for the code blocks and indentation.  
Note that the function prototype used in the declaration and definition is exactly the same.  

## Templates ##
### Short style ###
~~~c++
template < typename T > type myFunctionTemplate( type argument0, type argument1 )
	{
		// whatever you want
	}
~~~
### Long style ###
~~~c++
template < typename A, typename B, class C >
 	class myClassTemplate
		{
			// class declaration

		};
~~~
Template declaration style for both classes and functions follows the rules early adopted for the code blocks and indentation.  
Also there is a preference in the use of the **typename** and **class** keywords as template parameters types:  
 - The **typename** keyword is preferred if the template parameter is assumed to be a primitive type
 - The **class** keyword is preferred if the template parameter is assumed to be a class or a struct

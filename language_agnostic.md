# BEST PRACTICES

Always keep in mind:
- code is READ more often than it is written
- you might need to revisit your code years from now, will it make sense? Do yourself a favor and be clear
- someone else might need to read your code tomorrow, will it make sense? Do your colleagues a favor

## nmng cnvntns 

Please use vowels because:
- the great pixel shortage is over
- autocomplete is you friend
- code is read more often than it is written

If you have a dictionary(python) or json object that contains information about a hammer:
- do not put it into a variable named "dictionary" or "nail". Call it "hammer". 

Most of all be consistent with your naming conventions. If you join a new project then try to stick to whatever conventions are in place. This includes naming conventions and anything else.

## DRY - Dont Repeat Yourself Yourself

Ideally: every piece of knowledge should be represented in a code-base exactly once
- if you copy-paste buggy code then you have to fix all copies of it
- if you copy-paste code that is perfectly lekker and requirements change...
- dont repeat yourself
  
## Flat is better than nested

If you are ever tempted to put a loop inside a loop inside a loop inside of a ... etc. Rather dont. Make use of function definitions.

functions are: 
- more explicit 
- easier to test than the inner-most loop of a 5 loop stack of spagetti-code
- easier to document
- easier to reuse

## Explicit is better than implicit

You want the intention of code to be clear. You dont want anyone second-guessing your logic because they can't even tell what you were intending to do. So be explicit. Use comments if you have to, use sensible function, variable and class names. 

## The later an error is found, the more expensive it is to fix

- So be explicit in your code.
- Add "sanity checking" assertion statements
- Fail fast
- If you catch an exception be explicit about what you are trying to catch! Dont just silence errors, dont just write cryptic/useless messages to an output that nobody will read.
- write defensively, there are a lot of things that can go wrong

If an error happens then:
- you want to know it happened
- you want to now as much as possible about what went wrong

## Dont mix code and configuration

Configuration lives in:
- environmental variables
- settings files
- databases

Configuration can also be passed in as comand-line prameters if it makes senses

## Never Ever put passwords into the code base

especially if you are using version control

## Aways use version control

- See what I did there?
- Because it will save you
- we are all team players.

## Log with a logger

Just printing stuff out is ok for when you are prototyping your code, but production systems use proper logging systems. 

## KISS

Keep It Simple Stupid
- dont do fancy things for the sake of being fancy
- dont show off your l33t skillz

Aim for elegance. This means clarity and simplicity. The more moving parts you have in your code the more likely things will be to break

## Be specific in your code's requirements

If your app used `some_package==1.2.3` then that should be explicily recorded in a version-controlled file. Ideally it will be recorded in a file that your package manager can understand. 

## YAGNI

You aint gonna need it. see KISS. Don't build bells and whistles because you are feeling creative. It'll bite you later. Stay away from premature optimisations.

## Global variables

No

## small units

- If a function is more than 30 lines of code consider breaking it down 
- if you keep using the word "and" when describing a function then consider breaking it down. "This function does this and that andthis other thing..."

## Try to keep your code testible

- Don’t do work in object constructors, which are hard to test and surprising
- All theabove points
  
and please dont duplicate your logic in your test. Because, did I mention, DRY?

## Dont let perfect be the enemy of the good

Sometimes it isnecessary to incur technical debt. But debt is debt. You will pay interest in the form of slower development time the next time anyone works on the system. 

Sometimes there are special cases. Practicality beats purity. But dont be lazy, try to follow the rules

## Use the language that your users are using

Eg if you are writing a program for a training organisation that refers to its students as "recruits" then dont make a "Student" class, dont make a "Learner" class. A "Recruit" class migt be a good idea though. 

## Write loosely coupled code 

Production code doesn't stand still. It gets updated. New features are implemented, it gets refactored, potions get completely pulled out and re-created fster, better, stronger.

Your code should expose a few well defined public interfaces. If client code isn't supposed to touch a variable/method/object/whatever then use language standard practices to hide that  stuff, or at least make it obvious that it's not meant to be directly accessed.


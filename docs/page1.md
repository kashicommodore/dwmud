## Discworld MUD Guide

### Aliases and Nicknames

#### What are Aliases?
Basically, aliases are a way to make your own commands. Usually what this means is to make long and hard to type commands shorter. 
But you can also chain up many commands together, or simplify short, repetitive tasks.

#### How do you make an Alias?
```
alias <name> <command> 
```
for example
```
alias helloworld shout hello world I made an alias 
```
will make a helloworld command, which makes your character shout

#### Basic aliases
Lets get to the basics of what you need to get by.
Of course, feel free to adjust these to suit yourself.

First, lets simply make the kill command shorter.
`alias k kill $*$`

This will mean you can type `k rat` instead of `kill rat` in future. Quicker, no?  
*The `$*$` bit means 'anything I typed after the alias goes here'. So `k sailor` becomes `kill sailor`. Geddit?*  

To make aliases easier to list and browse in-game later, we can put them in categories too.  
`alias set category k General`  
Will put this alias in a new 'General' category.  

Lets try something else.
The consider command allows you to weigh up an opponent before you bash heads and swords. This can save you getting killed by enemies much tougher than you.
```
alias c consider $arg:all$
alias set category c General
```

So `c rat` will `consider rat`. Easy.  
*The `$arg:all$` bit means either 'use the word I put after the alias' (`c rat` becomes `consider rat`)...*  
*OR if I did not use any word - use 'all' instead. (`c` becomes `consider all`)*  

I like to make variants of this command to quickly consider my target (who I am already fighting), or the wounded too. Try these.
```
alias ca consider all
alias set category ca General
alias ct consider target
alias set category ct General
alias cw consider wounded
alias set category cw General
```

Another useful one is the 'health' command, which guages an opponents, or a friends, current health. See who is injured!

```
alias h health $arg:me$
alias set category h General
alias ha health all
alias set category ha General
alias ht health target
alias set category ht General
alias hw health wounded
alias set category hw General
```

# Underscore.strings #

Idea: Esa-Matti Suuronen (esa-matti aet suuronen dot org)

Authors: Esa-Matti Suuronen, Edward Tsech

Javascript lacks complete string manipulation operations.
This an attempt to fill that cap. List of buildin methods can be found
for example from [Dive Into JavaScript][d].

[d]: http://www.diveintojavascript.com/core-javascript-reference/the-string-object 


As name states this an extension for [Underscore.js][u], but it can be used
independently from **_s**-global variable. But with Underscore.js you can
use Object-Oriented style and chaining:

[u]: http://documentcloud.github.com/underscore/

    _("   epeli  ").chain().trim().capitalize().value()
    => "Epeli"


## String Functions ##

**blank** _.blank(string)

Checks if the string is empty or contains whitespaces only.

    _.blank(' ')
    => true

**capitalize** _.capitalize(string)

Converts first letter of the string to uppercase.

    _.capitalize("epeli")
    => "Epeli"
    
**chop** _.chop(string, step)

    _.chop('whitespace', 3)
    => ['whi','tes','pac','e']
    
**clean** _.clean(str)

Compress some whitespaces to one.

    _.clean(" foo    bar   ")
    => 'foo bar'
    
**contains** _.contains(string, substring)

Tests if string contains a substring.

    _.contains("foobar", "ob")
    => true

**count** _.count(string, substring)

    _('Hello world').count('l')
    => 3
    
**empty** _.empty(string)

    _('').empty()
    => true
    
**escapeHTML** _.escapeHTML(string)

Converts HTML special characters to their entity equivalents.

    _('<div>Blah blah blah</div>').escapeHTML();
    => '&lt;div&gt;Blah blah blah&lt;/div&gt;'
    
**includes** alias for *contains*.
    
**insert** _.insert(string, index, substing)

    _('Hello ').insert(6, 'world')
    => 'Hello world'

**join** _.join(separator, *strings)

Joins strings together with given separator

    _.join(" ", "foo", "bar")
    => "foo bar"
    
**reverse** _.reverse(string)

Reverses the string.

    _.reverse("foobar")
    => "raboof"

**splice**  _.splice(string, index, howmany, substring)

Like a array splice.

    _('https://edtsech@bitbucket.org/edtsech/underscore.strings').splice(30, 7, 'epeli')
    => 'https://edtsech@bitbucket.org/epeli/underscore.strings'
    
**startsWith** _.startsWith(string, starts)

This method checks whether string starts with starts.

    _("image.gif").startsWith("image")
    => true
    
**endsWith** _.endsWith(string, ends)

This method checks whether string ends with ends.

    _("image.gif").endsWith("gif")
    => true
    
**succ**  _.succ(str)

Returns the successor to str.

    _('a').succ()
    => 'b'
    
    _('A').succ()
    => 'B'
    
**supplant** 

Supplant function was removed, use Underscore.js template function.
[o]: http://documentcloud.github.com/underscore/#template
    
**strip** alias for *trim*

**lstrip** alias for *ltrim*

**rstrip** alias for *rtrim*

**titleize** _.titleize(string)

    _('my name is epeli').titleize()
    => 'My Name Is Epeli'
    
**trim** _.trim(string, [characters])

trims defined characters from begining and ending of the string.
Defaults to whitespace characters.

    _.trim("  foobar   ")
    => "foobar"

    _.trim("_-foobar-_", "_-")
    => "foobar"


**ltrim** _.ltrim(string, [characters])

Left trim. Similar to trim, but only for left side.


**rtrim** _.rtrim(string, [characters])

Left trim. Similar to trim, but only for right side.
    
**truncate** _.truncate(string, length, truncateString)

    _('Hello world').truncate(5)
    => 'Hello...'

**sprintf** _.sprintf(string format, *arguments)

C like string formatting. 
Credits goes to [Alexandru Marasteanu][o].
For more detailed documentation, see the [original page][o].

[o]: http://www.diveintojavascript.com/projects/sprintf-for-javascript

    _.sprintf("%.1f", 1.17)
    "1.2"


Any suggestions or bug reports are welcome. Just email me or more preferably open an issue.

# phpDocBlocks
PHP Doc Block Comment

### To set Up Auto Comments
Open File -> Settings -> Editor -> File and Code Templates -> Includes

Find:
PHP Function Doc Comment:

Replace with the following: 

```
#set( $regex = "([a-z])([A-Z]+)")
#set( $replacement = "$1 $2")
#set( $toSplit = $NAME.replaceAll($regex, $replacement))
#set( $toCapital = ${StringUtils.capitalizeFirstLetter($toSplit)})
...
/**
${toCapital}
 * 
#if (${PARAM_DOC} != "") ${PARAM_DOC}
 *
#end
 * @author AC a.clark@email.co.uk
#if (${TYPE_HINT} != "void")
 *
 * @return ${TYPE_HINT}
#end
#if (${THROWS_DOC} != "") 
 *
${THROWS_DOC}
#end
*/
```

### To Use
When coding, click the cursor onto the function name, hold the ALT key and press Return.  This should pop up a list of options, one being "Generate PHP Doc For Function"  Select this and the Doc Block Comments will be generated as set above.

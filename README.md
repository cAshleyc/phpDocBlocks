# phpDocBlocks
PHP Doc Block Comment

File -> Settings -> Editor -> File and Code Templates -> Includes

PHP Function Doc Comment:

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

# XAJAX_PHP8
XAJAX funcional con PHP > 7.2

Deprecated: Function get_magic_quotes_gpc() is deprecated in xajax/xajax/xajax_core/xajaxArgumentManager.inc.php on line 247
Se comenta la linea 247
// if (1 == get_magic_quotes_gpc())
   array_walk($this->aArgs, array(&$this, '__argumentStripSlashes'));


Deprecated: strlen(): Passing null to parameter #1 ($string) of type string is deprecated in xajax/xajax/xajax_core/plugin_layer/support/xajaxUserFunction.inc.php on line 177

Agrego comprobacion isset para que no pueda ser null
if ( 0 < strlen($this->sAlias))
lo dejo
if (isset($this->sAlias) && 0 < strlen($this->sAlias))

A partir de aqui se cambian los constructores de todas las clases para que en vez de ser el nombre de la propia clase sea
__construct para que funcione con versiones modernas, como en el ejemplo que sigue.

xajax/xajax/xajax_core/xajaxRequest.inc.php on line 291
Se cambia el contructor en la linea 315 por __construct
function __construct($sScript)
{
	$this->aVariables = array();
	$this->sScript = $sScript;
}

Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; xajaxScriptPlugin has a deprecated constructor in xajax/xajax/xajax_core/plugin_layer/xajaxScriptPlugin.inc.php on line 29
se cambia el constructor 

Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; xajaxEventPlugin has a deprecated constructor in xajax/xajax/xajax_core/plugin_layer/xajaxEventPlugin.inc.php on line 43
se cambia el constructor

Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; xajaxIncludeClientScriptPlugin has a deprecated constructor in xajax\xajax_core\plugin_layer\xajaxDefaultIncludePlugin.inc.php on line 29
se cambia el constructor

 Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; xajaxUserFunction has a deprecated constructor in xajax\xajax_core\plugin_layer\support\xajaxUserFunction.inc.php on line 31
 se cambia el constructor
 
 Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; xajaxFunctionPlugin has a deprecated constructor in xajax\xajax_core\plugin_layer\xajaxFunctionPlugin.inc.php on line 37
 se cambia el constructor
 
 Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; xajaxFunctionPlugin has a deprecated constructor in xajax/xajax_core/plugin_layer/xajaxFunctionPlugin.inc.php on line 37
  se cambia el constructor

Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; xajaxUserFunction has a deprecated constructor in xajax/xajax_core/plugin_layer/support/xajaxUserFunction.inc.php on line 31
  se cambia el constructor

Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; xajaxIncludeClientScriptPlugin has a deprecated constructor in xajax/xajax_core/plugin_layer/xajaxDefaultIncludePlugin.inc.php on line 29
se cambia el constructor
 
 
 

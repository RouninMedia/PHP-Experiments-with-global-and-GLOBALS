# PHP Experiments with `global` and `$GLOBALS`
A temporary repository while I get my head around the PHP `global` keyword and `$GLOBALS` superglobal.

## Experiment

```php

${'<My_Test>'} = ['Test1' => 'Test2'];

function myFunction($String, $Capsule) {

  // print_r($GLOBALS);

  // echo 'Function working';
  
  // PRINT CAPSULE
  print_r($Capsule);

  // global KEYWORD
  global ${'<'.$String.'>'};
  
  if (isset(${'<'.$String.'>'})) {
      
    print_r(${'<'.$String.'>'});
  }

  // $GLOBALS SUPERGLOBAL
  if (isset($GLOBALS['<'.$String.'>'])) {
      
    print_r($GLOBALS['<'.$String.'>']);
  }
}

myFunction('My_Test', ${'<My_Test>'});

```

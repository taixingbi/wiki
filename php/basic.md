### =>
create an associative array

    <?php
    $age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");
    echo "Peter is " . $age['Peter'] . " years old.";
    ?>
        
### ->
property

    <?php
    class SimpleClass
    {
        // property declaration
        public $var = 'a default value';

        // method declaration
        public function displayVar() {
            echo $this->var;
        }
    }
    ?>
    
### ::
Scope Resolution Operator 

* outside

        <?php
        class MyClass {
            const CONST_VALUE = 'A constant value';
        }

        $classname = 'MyClass';
        echo $classname::CONST_VALUE; // As of PHP 5.3.0

        echo MyClass::CONST_VALUE;
        ?>
        
* inside

        <?php
        class OtherClass extends MyClass
        {
            public static $my_static = 'static var';

            public static function doubleColon() {
                echo parent::CONST_VALUE . "\n";
                echo self::$my_static . "\n";
            }
        }

        $classname = 'OtherClass';
        $classname::doubleColon(); // As of PHP 5.3.0

        OtherClass::doubleColon();
        ?>









  




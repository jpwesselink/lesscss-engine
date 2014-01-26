LESS Engine
===========

LESS Engine provides basic access to the core LESS functionality. It's a core library that 
can be used for a variety of JVM based LESS applications.

### Caveat emptor

Yes, in order to use multiple versions of less alongside eachother I raped the com.asual.lesscss namespace by postfixing it with the less version. Pretty? No. Works? Yes.
It does not come with any support nor any promise that it will have the same functionality as Asual's future releases. 




Usage
-----

The following sample demonstrates how the API can be used to parse strings and
compile URL resources:

    // Instantiates a new LessEngine
    LessEngine engine = new LessEngine();
    
    // Compiles a CSS string
    String text = engine.compile("div { width: 1 + 1 }");

    // Compiles an URL resource
    String url = engine.compile(getClass().getClassLoader().getResource("META-INF/test.css"));

    // Creates a new file containing the compiled content
    engine.compile(new File("/Users/User/Projects/styles.less"), 
                   new File("/Users/User/Projects/styles.css"));

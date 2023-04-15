# Angular
angular prep

is Angular MVC or MVVM?

Angular is a Model-View-Controller (MVC) framework. The core architecture of Angular is based on the MVC pattern, where the Model represents the data and business logic, the View represents the UI elements, and the Controller acts as an intermediary between the Model and View, handling user input and updating the Model and View accordingly.

However, Angular also incorporates some elements of the Model-View-ViewModel (MVVM) pattern, particularly in its use of templates and data binding. In MVVM, the ViewModel acts as an intermediary between the View and Model, and facilitates data binding between the two.

So, while Angular is primarily an MVC framework, it does incorporate some MVVM principles.
-----------------------------------------------------------------------------------------------------
=====================================================================================================
AOT and JIT

AOT and JIT are two different modes of compilation in Angular, with different benefits and trade-offs.

AOT (Ahead-of-Time) compilation generates compiled code during the build process, before the code is served to the browser. 
JIT (Just-in-Time) compilation, on the other hand, compiles the code in the browser at runtime.

Here are the step-by-step compilation processes for AOT and JIT in Angular:

AOT Compilation:

The developer writes the code in TypeScript and creates templates using Angular's template syntax.
The Angular Compiler compiles the templates and generates JavaScript code.
The TypeScript compiler compiles the TypeScript code into JavaScript code.
The AOT compiler generates compiled code during the build process, including the templates, components, and metadata, which is then bundled and sent to the browser.
When the browser receives the code, it does not need to compile the code again, which makes the application load faster and improves performance.

JIT Compilation:

The developer writes the code in TypeScript and creates templates using Angular's template syntax.
The Angular Compiler compiles the templates and generates JavaScript code.
The TypeScript compiler compiles the TypeScript code into JavaScript code.
When the application is served to the browser, the JIT compiler runs in the browser and compiles the code at runtime.
The compiled code is executed by the browser, and the application runs as expected.
The main benefit of AOT compilation is improved performance, as the compiled code is already optimized before it reaches the browser. This makes the application load faster and perform better. On the other hand, JIT compilation allows for faster development and easier debugging, as the code can be recompiled on the fly as needed.

In summary, AOT and JIT are two different modes of compilation in Angular, with different benefits and trade-offs. AOT generates compiled code during the build process, while JIT compiles the code in the browser at runtime. Both modes of compilation have their own advantages and disadvantages, and the choice depends on the specific needs of the application.
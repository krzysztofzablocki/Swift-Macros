# Swift Macros :rocket:
<img align="left" width="256" height="256" src="https://github.com/krzysztofzablocki/Swift-Macros/blob/d218dea43b205e1c002feb28610d58d2c4d105dc/Icon.png">
</br></br>

Swift Macros have brought in a new wave of possibilities. The aim of this project is to curate a list of community-created Macros and associated learning resources. 

A lot of use-cases my [Sourcery](https://github.com/krzysztofzablocki/Sourcery) covered before can now be implemented by Swift Macros.

<br/><br/><br/><br/><br/>


## Learning Resources :books:

### **Tools**
- [Swift AST Explorer](https://swift-ast-explorer.com/)
  - This is extremely helpful when working with [SwiftSyntax](https://github.com/apple/swift-syntax), I used this when writing [Sourcery](https://github.com/krzysztofzablocki/Sourcery) parser and you can leverage it to build your own Macros. 

### **Apple:**

Dive into Swift Macros with these WWDC sessions:

- [Write Swift Macros](https://developer.apple.com/videos/play/wwdc2023-10166): An introductory session on Macros, their roles, and workings with a basic example.
- [Expand Swift Macros](https://developer.apple.com/videos/play/wwdc2023-10167): A deeper exploration into crafting your Macros and testing their functionality.

Other Apple Resources:

- [Macros](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/macros): The Official Step-by-Step Guide to Using Macros for Compile-Time Code Generation in Swift.
- [Example Swift Macros](https://github.com/DougGregor/swift-macro-examples): Check out real-world examples from Apple, like `@AddCompletionHandler` and `@AddAsync`.

### **Community Blogs**
- [Swift Macros by SwiftLee](https://www.avanderlee.com/swift/macros/)
  - Antoine goes over the introduction of what Macros are and how you can build your own one with an example.
- [How to Create Swift Macros in Xcode 15](https://blog.leonifrancesco.com/articles/swift-macros)
  - Francesco goes over creating your first macro with testing and some interesting tidbits.
- [Exploring Swift Macros](https://medium.com/dev-genius/exploring-new-swift-macros-api-245e0b1f7c8d)
  - Sergey goes over creating a macro for a memberwise initaliser step by step with tests and convenience methods for SwiftSyntax
- [Automating RawRepresentable Conformance with Swift Macros](https://otbivnoe.ru/2023/06/13/Automating-RawRepresentable-Conformance-with-Swift-Macros.html)
  - Nikita goes over creating a macro for automating the String RawRepresentable conformance.
---

## Macros :computer:

### SwiftUI
- [EnvironmentValues & EnvironmentValue](https://github.com/Wouter01/SwiftUI-Macros/tree/main): Bypass boilerplate code and swiftly support new SwiftUI Environment Keys and Values.
- [SFSymbols Macro](https://github.com/lukepistrol/SFSymbolsMacro): A Swift Macro for "type-safe" SF Symbols.

### Models
- [Coding Keys](https://github.com/Ryu0118/CodingKeysMacro): Effortlessly generate CodingKeys for converting `snake_case` to `lowerCamelCase`.
- [Builder pattern](https://github.com/dziobaczy/SwiftBuilderMacro): Apply the [Builder Pattern](https://refactoring.guru/design-patterns/builder) with ease by generating a `Builder` helper class, mimicking stored properties of the associated struct.
- [EnhancedMirror](https://github.com/unixzii/EnhancedMirror): An experimental Mirror alternative that utilizes Swift Macros for static reflection.

### Testing
- [Power Assert](https://github.com/kishikawakatsumi/swift-power-assert): Adds assertions that can automatically produce information about the values being evaluated, and present it in an easily digestible form.
- [Spyable](https://github.com/Matejkob/swift-spyable): A Swift macro that simplifies and automates the process of creating spies for testing. Using the `@Spyable` annotation on a protocol, the macro generates a spy class 
that implements the same interface as the protocol and keeps track of interactions with its methods and properties.

### Networking
- [SwiftRequest](https://github.com/ailtonvivaz/swift-request): SwiftRequest is a lightweight, type-safe HTTP client for Swift, streamlining the construction and execution of HTTP request build on top of Macros.

### Enums
- [ExtractCaseValue](https://github.com/fruitcoder/extract-case-value): A Swift macro that extracts associated values from enum cases.

### Utility
- [AssociatedObject](https://github.com/p-x9/AssociatedObject): A Swift Macro for adding stored properties in Extension to classes defined in external modules, etc.  
  (This is implemented by wrapping `objc_getAssociatedObject`/`objc_setAssociatedObject`.)

### Misc
- [MacroKit](https://github.com/IanKeen/MacroKit): A collection of macros including:
  - `@PublicInit`: Generate public memberwise init
  - `@GenerateMock`: Create a mock object for testing from a protocol
  - `@KeyPathIterable`: Like `CaseIterable` but for available keypaths on a type
  - `@StaticMemberIterable`: Like `CaseIterable` but for available static members on a type
  - More to come...
- [InitMacro](https://github.com/LeonardoCardoso/InitMacro): A Swift Macro implementation that generates initializers for classes and structs with support for default values, wildcards and access control.
---

_**Take part in this exciting evolution in Swift. Your contributions are most welcome!**_

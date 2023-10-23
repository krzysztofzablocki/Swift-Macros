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

### **Frameworks**

- [Swift Macro Testing](https://github.com/pointfreeco/swift-macro-testing): Magical testing tools for Swift macros.
  - Provides `assertMacro`, an alternative to Apple's `assertMacroExpansion` that automatically snapshots macro expansions.
  - Also provides string-based matching for diagnostics and fix-its instead of manually specifying line and column numbers.

### **Apple:**

Dive into Swift Macros with these WWDC sessions:

- [Write Swift Macros](https://developer.apple.com/videos/play/wwdc2023-10166): An introductory session on Macros, their roles, and workings with a basic example.
- [Expand Swift Macros](https://developer.apple.com/videos/play/wwdc2023-10167): A deeper exploration into crafting your Macros and testing their functionality.

Other Apple Resources:

- [Macros](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/macros): The Official Step-by-Step Guide to Using Macros for Compile-Time Code Generation in Swift.
- [Example Swift Macros](https://github.com/apple/swift-syntax/tree/main/Examples/Sources/MacroExamples): Check out real-world examples from Apple, like `@AddCompletionHandler` and `@AddAsync`.

### **Community Blogs**
- [Swift Macros by SwiftLee](https://www.avanderlee.com/swift/macros/)
  - Antoine goes over the introduction of what Macros are and how you can build your own one with an example.
- [How to Create Swift Macros in Xcode 15](https://blog.leonifrancesco.com/articles/swift-macros)
  - Francesco goes over creating your first macro with testing and some interesting tidbits.
- [Exploring Swift Macros](https://medium.com/dev-genius/exploring-new-swift-macros-api-245e0b1f7c8d)
  - Sergey goes over creating a macro for a memberwise initaliser step by step with tests and convenience methods for SwiftSyntax
- [Automating RawRepresentable Conformance with Swift Macros](https://otbivnoe.ru/2023/06/13/Automating-RawRepresentable-Conformance-with-Swift-Macros.html)
  - Nikita goes over creating a macro for automating the String RawRepresentable conformance.
- [Setup to develop Swift Macros](https://medium.com/@tim_wang/setup-to-develop-swift-macros-68d8fe2fea59)
  - A step-by-step tutorial to develop Swift Macros.
---

## Macros :computer:

### SwiftUI
- [EnvironmentValues & EnvironmentValue](https://github.com/Wouter01/SwiftUI-Macros/tree/main): Bypass boilerplate code and swiftly support new SwiftUI Environment Keys and Values.
- [SFSymbols Macro](https://github.com/lukepistrol/SFSymbolsMacro): A Swift Macro for "type-safe" SF Symbols.
- [SF Symbols Generator](https://github.com/zijievv/sf-symbols-generator): A Swift macro generating type-safe SF Symbols.
- [Prototype (WIP)](https://github.com/mrylmz/Prototype): Prototype generates SwiftUI Forms and Views for data structures and classes, designed to complement SwiftData Models seamlessly.
- [HexColors](https://github.com/alvmo/HexColors): Swift Macros for validating hex colors from string and hexadecimal integer literals.

### Models
- [Coding Keys](https://github.com/Ryu0118/CodingKeysMacro): Effortlessly generate CodingKeys for converting `snake_case` to `lowerCamelCase`.
- [Coding Keys](https://github.com/sasha-riabchuk/CodingKeysMacro-swift): A Swift Macro for automating CodingKeys creation in Codable structs. Supports custom string mappings for properties.
- [Coding Keys](https://github.com/zijievv/CodingKeysGenerator): Swift macros generating customizable `CodingKeys`.
- [Builder pattern](https://github.com/dziobaczy/SwiftBuilderMacro): Apply the [Builder Pattern](https://refactoring.guru/design-patterns/builder) with ease by generating a `Builder` helper class, mimicking stored properties of the associated struct.
- [Struct Builder Macro](https://github.com/alschmut/StructBuilderMacro): An attached macro that produces a peer struct which implements the builder pattern. This allows the creation of the struct with minimal effort using default values.
- [EnhancedMirror](https://github.com/unixzii/EnhancedMirror): An experimental Mirror alternative that utilizes Swift Macros for static reflection.
- [MetaCodable](https://github.com/SwiftyLab/MetaCodable): Generates `Codable` implementation with following features:
  - Allows custom `CodingKey` value declaration per variable, instead of requiring you to write for all fields.
  - Allows to create flattened model for nested `CodingKey` values.
  - Allows to create composition of multiple `Codable` types.
  - Allows to provide default value **in case of decoding failures**.
  - Generates member-wise initializer **considering the default values**.
  - Allows to create custom decoding/encoding strategies. 
- [Sealed](https://github.com/leedh2004/SealedMacro): Parsing easily Sealed Class JSON Model on Server. (ex. kotlin server)
- [MacroCodableKit](https://github.com/mikhailmaslo/macro-codable-kit): Fully self-sufficient `Codable` kit:
   - Implements OpenAPI [allOf](https://spec.openapis.org/oas/v3.1.0#composition-and-inheritance-polymorphism) and [oneOf](https://spec.openapis.org/oas/v3.1.0#fixed-fields-20) specs
   - Adjusts coding keys with a simple `@CodingKey` annotation
   - Decodes arrays and dictionaries in a safe manner with `@CustomCoding(SafeDecoding)`
   - Has built-in per-property `Codable` strategies and is extendible for new ones.

### Dependency Injection
- [swift-blade](https://github.com/shackley/swift-blade): A macro powered dependency injection framework.
- [MDI](https://github.com/renato-iar/MDI): High performance dependency injection framework.

### Testing
- [Power Assert](https://github.com/kishikawakatsumi/swift-power-assert): Adds assertions that can automatically produce information about the values being evaluated, and present it in an easily digestible form.
- [Spyable](https://github.com/Matejkob/swift-spyable): A Swift macro that simplifies and automates the process of creating spies for testing. Using the `@Spyable` annotation on a protocol, the macro generates a spy class 
that implements the same interface as the protocol and keeps track of interactions with its methods and properties.
- [SwiftMock](https://github.com/MetalheadSanya/swift-mock): A Swift framework that simplifies and automates the process of creating mock objects for testing. Using the `@Mock` macro on a protocol generates Mock class. You can stub methods and properties, verifying mock calls.

### Networking
- [SwiftRequest](https://github.com/ailtonvivaz/swift-request): SwiftRequest is a lightweight, type-safe HTTP client for Swift, streamlining the construction and execution of HTTP request build on top of Macros.
- [Papyrus](https://github.com/joshuawright11/papyrus): A type-safe, protocol based HTTP client - turn your APIs into Swift protocols. Includes first-class testing support with out of the box mocking.

### Enums
- [ExtractCaseValue](https://github.com/fruitcoder/extract-case-value): A Swift macro that extracts associated values from enum cases.

### Misc
- [MacroKit](https://github.com/IanKeen/MacroKit): A collection of macros including:
  - `@PublicInit`: Generate public memberwise init
  - `@GenerateMock`: Create a mock object for testing from a protocol
  - `@KeyPathIterable`: Like `CaseIterable` but for available keypaths on a type
  - `@StaticMemberIterable`: Like `CaseIterable` but for available static members on a type
  - More to come...
- [InitMacro](https://github.com/LeonardoCardoso/InitMacro): A Swift Macro implementation that generates initializers for classes and structs with support for default values, wildcards and access control.
- [AssociatedObject](https://github.com/p-x9/AssociatedObject): A Swift Macro for adding stored properties in Extension to classes defined in external modules, etc.  
  (This is implemented by wrapping `objc_getAssociatedObject`/`objc_setAssociatedObject`.)
- [AssociatedObjectMacro](https://github.com/syt2/AssociatedObjectMacro): A Swift Macro for convenient declaration of variables in class extensions.
- [AliasMacro](https://github.com/p-x9/AliasMacro): A Swift Macro for defining aliases for types, functions, or variables.
- [UtilityType](https://github.com/bannzai/UtilityType): UtilityType is an innovative library designed to realize TypeScript's UtilityTypes in Swift. See more details: https://www.typescriptlang.org/docs/handbook/utility-types.html
  - `@Partial`,`@Required`: Constructs a type with all properties set to optional(`@Partial`) or require(`@Required`). This utility will return a type that represents all subsets of a given type.
  - `@Pick`,`@Omit`: Constructs a type by picking(`@Pick`) or removing(`@Omit`) the set of specific properties keys (only string literal) from attached Type.
  - `@Exclude`,`@Extract`: Constructs a type by excluding(`@Exclude`) or extracting(`@Extract`) from enum all cases.
  - `@Parameters`: Constructs a tuple type from the types used in the parameters of a function type.
  - `@ReturnType`: Constructs a type consisting of the return type of function.
- [Reuse Identifier](https://github.com/collisionspace/ReuseIdentifierMacro): A Reuse Identifier Macro that is useful in generation of a reuse id for your UICollectionViewCells and UITableViewCells
- [SwiftMacros collection](https://github.com/ShenghaiWang/SwiftMacros): A practical collection of Swift Macros that help code correctly and smartly.
- [ModifiedCopyMacro](https://github.com/WilhelmOks/ModifiedCopyMacro): A Swift macro for making inline copies of a struct by modifying a property.
- [DictionaryLiteralShorthandMacro](https://github.com/Dcard/DictionaryLiteralShorthandMacro): A Swfit macro for creating dictionary literals with keys as "string representations of corresponding variable names".
- [TemporaryVariable](https://github.com/yume190/TemporaryVariable): `TemporaryVariable` provide a macro `#info {...}`. It capture most function calls and assign them to temporary variables.
- [Localizable](https://github.com/ADiks09/Localizable): `Localizable` A macro that produces variables and methods, for your localization files. From the enumeration keys.
- [SafeDecoding](https://github.com/renato-iar/SafeDecoding): `SafeDecoding` A macro that implements failable decoding via custom initializer; allows auto-conformance to `Decodable`` and per-property opt-out.

---

_**Take part in this exciting evolution in Swift. Your contributions are most welcome!**_

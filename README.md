# Swift Macros :rocket:
<img align="left" width="256" height="256" src="https://github.com/krzysztofzablocki/Swift-Macros/blob/d218dea43b205e1c002feb28610d58d2c4d105dc/Icon.png">
</br></br>

Swift Macros have brought in a new wave of possibilities. The aim of this project is to curate a list of community-created Macros and associated learning resources. 

A lot of use-cases my [Sourcery](https://github.com/krzysztofzablocki/Sourcery) covered before can now be implemented by Swift Macros.

<br/><br/><br/><br/><br/>

[**If you'd like to support my work and improve your engineering workflows, check out my SwiftyStack course**](https://www.swiftystack.com/)

## Learning Resources :books:

### **Tools**
- [Swift AST Explorer](https://swift-ast-explorer.com/)
  - This is extremely helpful when working with [SwiftSyntax](https://github.com/apple/swift-syntax), I used this when writing [Sourcery](https://github.com/krzysztofzablocki/Sourcery) parser and you can leverage it to build your own Macros. 

### **Frameworks**

- [Swift Macro Testing](https://github.com/pointfreeco/swift-macro-testing): Magical testing tools for Swift macros.
  - Provides `assertMacro`, an alternative to Apple's `assertMacroExpansion` that automatically snapshots macro expansions.
  - Also provides string-based matching for diagnostics and fix-its instead of manually specifying line and column numbers.
- [Macro ToolKit](https://github.com/stackotter/swift-macro-toolkit)
  - A powerful toolkit for creating concise and expressive Swift macros.

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
- [Support Swift macros with CocoaPods](https://soumyamahunt.medium.com/support-swift-macros-with-cocoapods-3911f9317042)
  - Guide to distribute your macros using CocoaPods.
- [Deep Dive Into Macros by Coding With Vera](https://codingwithvera.com/deep-dive-into-macros/)
  - Vera goes into how Macros work with a real-life comparison. Also explains the different types of macros and how they can help your codebase.
- [How to Create Swift Macros: The Easiest and Least Boring Way](https://traderepublic.substack.com/p/how-to-create-swift-macros-the-easiest)
  - A step-by-step guide to building your first Swift macro from scratch, simple and straightforward. Learn the syntax, how to register a macro, how to test it, and more, all with practical examples.
---

## Macros :computer:

### SwiftUI
- [EnvironmentValues & EnvironmentValue](https://github.com/Wouter01/SwiftUI-Macros/tree/main): Bypass boilerplate code and swiftly support new SwiftUI Environment Keys and Values.
- [SFSymbols Macro](https://github.com/lukepistrol/SFSymbolsMacro): A Swift Macro for "type-safe" SF Symbols.
- [SF Symbols Generator](https://github.com/zijievv/sf-symbols-generator): A Swift macro generating type-safe SF Symbols.
- [Prototype (WIP)](https://github.com/mrylmz/Prototype): Prototype generates SwiftUI Forms and Views for data structures and classes, designed to complement SwiftData Models seamlessly.
- [HexColors](https://github.com/alvmo/HexColors): Swift Macros for validating hex colors from string and hexadecimal integer literals.
- [Equatable](https://github.com/ordo-one/equatable): A Swift Macros for generating Equatable conformances for structs for high performance SwiftUI view diffing.

### Models
- [Coding Keys](https://github.com/Ryu0118/CodingKeysMacro): Effortlessly generate CodingKeys for converting `snake_case` to `lowerCamelCase`.
- [Coding Keys](https://github.com/sasha-riabchuk/CodingKeysMacro-swift): A Swift Macro for automating CodingKeys creation in Codable structs. Supports custom string mappings for properties.
- [Coding Keys](https://github.com/zijievv/CodingKeysGenerator): Swift macros generating customizable `CodingKeys`.
- [Builder pattern](https://github.com/dziobaczy/SwiftBuilderMacro): Apply the [Builder Pattern](https://refactoring.guru/design-patterns/builder) with ease by generating a `Builder` helper class, mimicking stored properties of the associated struct.
- [Buildable Macro](https://github.com/alschmut/StructBuilderMacro): An attached macro for structs, classes and enums, which produces a peer struct implementing the builder pattern. Initialise your object with minimal effort using default values:
  ```swift
  @Buildable struct Person { ... }
  let person = PersonBuilder(age: 42).build()
  ```
- [EnhancedMirror](https://github.com/unixzii/EnhancedMirror): An experimental Mirror alternative that utilizes Swift Macros for static reflection.
- [MetaCodable](https://github.com/SwiftyLab/MetaCodable): Generates `Codable` implementation with following features:
  - Allows custom `CodingKey` value declaration per variable, instead of requiring you to write for all fields.
  - Allows to create flattened model for nested `CodingKey` values.
  - Allows to create composition of multiple `Codable` types.
  - Allows to provide default value **in case of decoding failures**.
  - Generates member-wise initializer **considering the default values**.
  - Allows to create custom decoding/encoding strategies.
  - Allows specifying fallback `CodingKey` values for fields and cases.
  - Allows to ignore specific properties/cases from decoding/encoding.
  - Allows setting `CodingKey` case style per type.
  - Allows decoding/encoding any type that conform to a particular protocol.
  - Allows decoding/encoding enums and protocols with external/internal/adjacent identifier.
  - Allows decoding/encoding enums and protocols with non-`String` identifier or customize the identifier detection.
- [Sealed](https://github.com/leedh2004/SealedMacro): Parsing easily Sealed Class JSON Model on Server. (ex. kotlin server)
- [MacroCodableKit](https://github.com/mikhailmaslo/macro-codable-kit): Fully self-sufficient `Codable` kit:
   - Implements OpenAPI [allOf](https://spec.openapis.org/oas/v3.1.0#composition-and-inheritance-polymorphism) and [oneOf](https://spec.openapis.org/oas/v3.1.0#fixed-fields-20) specs
   - Adjusts coding keys with a simple `@CodingKey` annotation
   - Decodes arrays and dictionaries in a safe manner with `@CustomCoding(SafeDecoding)`
   - Has built-in per-property `Codable` strategies and is extendible for new ones.
- [SampleBuilder](https://github.com/pitt500/SwiftAndTipsMacros#samplebuilder): The aim of @SampleBuilder is straightforward: Generate an array of sample data from your models for use in SwiftUI previews, unit tests, or any scenario that needs mock data—without the hassle of crafting it from scratch.It works with `structs` and `enums`!
  - [SampleBuilderItem](https://github.com/pitt500/SwiftAndTipsMacros#samplebuilderitem): If you want to customize your sample data even further for `.random` generator, you can use `@SampleBuilderItem` to specify the type of data you want to generate for each property in your model (images, prices, names, etc.).
- [CodableOptionSet](https://github.com/neothXT/CodableOptionSet): CodableOptionSet allows for easy extensions to OptionSets implementing Codable protocol.
- [ListableProperties](https://github.com/neothXT/ListableProperties): ListableProperties macro adds `getProperties` static func which returns an array of all property names in your model.
- [BuildableMacro](https://github.com/Mr-Alirezaa/BuildableMacro): A set of macros simplifying setter function generation for nominal types, inspired by SwiftUI modifiers and Observation framework macros:
  - [`@Buildable`](https://github.com/Mr-Alirezaa/BuildableMacro#buildable) Automates the marking of settable properties as `@BuildableTracked`, excluding those marked as `@BuildableIgnored`.
  - [`@BuildableTracked`](https://github.com/Mr-Alirezaa/BuildableMacro#buildabletracked) Generates setter functions for each marked property, allowing fluent chaining of modifications.
  - [`@BuildableIgnored`](https://github.com/Mr-Alirezaa/BuildableMacro#buildabletracked) Excludes properties from automatic setter function generation.
- [StaticArray](https://github.com/malien/StaticArray): An allocation-less C-like fixed size arrays.
- [UserDefaultsObservation](https://github.com/tgeisse/UserDefaultsObservation): Combines UserDefaults and the Observation Framework. Users can easily create an Observable class where properties are backed by UserDefaults and NSUbiquitousKeyValueStore.
- [LoremSwiftify](https://github.com/EnesKaraosman/LoremSwiftify): LoremSwiftify is a Macro that creates lorem ipsum data for your models.
- [SwiftCopyable](https://github.com/ugommirikwe/SwiftCopyableMacro): Auto-generates a `copy` function for structs, making it easy to duplicate a struct instance while updating its properties with new values, similar to what Kotlin `data class` offers.

### Dependency Injection
- [swift-blade](https://github.com/shackley/swift-blade): A macro powered dependency injection framework.
- [MDI](https://github.com/renato-iar/MDI): High performance dependency injection framework.
- [SwiftEnvironment](https://github.com/hainayanda/SwiftEnvironment): SwiftUI based Environment global dependency locator framework with macro.
- [SafeDI](https://github.com/dfed/SafeDI): Compile-time safe dependency injection via code generation.
- [Stitch](https://github.com/entrhq/stitch): A lightweight, SwiftUI inspired, compile time safe dependency injection library fully integrated into the SwiftUI lifecycle and compatible with view composition updates.
- [Crocodil](https://github.com/KazaiMazai/Crocodil): Elegant dependency injection with Swift Macro

### Testing
- [Testable](https://github.com/fernandolucheti/TestableMacro): A macro that produces tests hooks on DEBUG builds to allow testing private methods and properties.
- [Mockable](https://github.com/Kolos65/Mockable): Provides automatic mock implementations for your protocols and an intuitive syntax that simplifies the process of mocking services and verifying invocations in your unit tests.
- [Power Assert](https://github.com/kishikawakatsumi/swift-power-assert): Adds assertions that can automatically produce information about the values being evaluated, and present it in an easily digestible form.
- [Spyable](https://github.com/Matejkob/swift-spyable): A Swift macro that simplifies and automates the process of creating spies for testing. Using the `@Spyable` annotation on a protocol, the macro generates a spy class 
that implements the same interface as the protocol and keeps track of interactions with its methods and properties.
- [SwiftMock](https://github.com/MetalheadSanya/swift-mock): A Swift framework that simplifies and automates the process of creating mock objects for testing. Using the `@Mock` macro on a protocol generates Mock class. You can stub methods and properties, verifying mock calls.
- [XCTestParametrizedMacro](https://github.com/PGSSoft/XCTestParametrizedMacro): A Swift macro that greatly simplifies testing for many parameters. It will allow you to write one test method and parametrize it with many cases. Use `@Parametrize(input: ["any", "values"])` to automatically generate new test methods for all parameters.

### Networking
- [SwiftRequest](https://github.com/ailtonvivaz/swift-request): SwiftRequest is a lightweight, type-safe HTTP client for Swift, streamlining the construction and execution of HTTP request build on top of Macros.
- [Papyrus](https://github.com/joshuawright11/papyrus): A type-safe, protocol based HTTP client - turn your APIs into Swift protocols. Includes first-class testing support with out of the box mocking.
- [SwiftNet](https://github.com/neothXT/SwiftNet): SwiftNet allows to create complex network request with built-in SSL/Certificate pinning, safe access token storage, automatic callback mechanism and the ability to build those requests as Combine's Publishers as well as Async/Await tasks. Framework also provides methods to test your requests easily with or without response model checks.
- [Snowdrop](https://github.com/neothXT/Snowdrop): Super lightweight, type-safe, protocol based framework that includes simple and fast out of the box mocking, SSL/Certificate pinning, interception mechanism and the path variable default value support to bypass Swift protocol's limitations.

### Enums
- [CasePaths](https://github.com/pointfreeco/swift-case-paths): `@CasePathable` produces key paths for enum cases, allowing enums to be used in dynamic member lookup and other generic algorithms.
- [ExtractCaseValue](https://github.com/fruitcoder/extract-case-value): A Swift macro that extracts associated values from enum cases.
- [EnumeratorMacro](https://github.com/MahdiBM/enumerator-macro): Generate custom code for your enums using Mustache templates.
- [EnumRawValues](https://github.com/DnV1eX/EnumRawValues): Enables full-fledged raw values for enums, supporting any equatable raw value types, assigning raw values with constants, expressions and more.
- [EnumOptionSet](https://github.com/DnV1eX/EnumOptionSet): Enables more concise and safer declaration of option sets through enumeration notation.
- [CaseEquatable](https://github.com/jakkornat/CaseEquatable): Automatically generates a “raw” case-only enumeration and makes your enum conform to `CaseEquatable`. This allows you to compare only the case names—ignoring any associated values.
- [QuickEnum](https://github.com/jeffreykuiken/QuickEnum): Quickly generate a simple enum based on a property's type and a list of cases that you provide

### Misc
- [Protocol](https://github.com/fernandolucheti/ProtocolMacro.git): A macro that produces a protocol based on a class/struct public interface.
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
- [Localize](https://github.com/Mackarous/Localize): `#Localize` An inline (freestanding) macro that expands to `LocalizedStringResource` and works within Swift packages.
- [TranslateKit SDK](https://github.com/FlineDev/TranslateKit): A Swift localization framework that simplifies app translation with macros and pre-localized strings.
  - `#tk("Save Changes")` automatically generates a **semantic localization key** instead of hardcoding strings.
  - **2000+ pre-localized strings** in ~40 languages, covering common UI text without adding them to a String Catalog.
  - **Autocompletion support** in Xcode makes discovering the right translation easy.
  - **Category-specific extensions** for App Store app types (Finance, Health, Productivity, etc.).
  - **Supports Swift Packages** with `#tkm`, ensuring correct key resolution inside SPM modules.
- [SafeDecoding](https://github.com/renato-iar/SafeDecoding): `SafeDecoding` A macro that implements failable decoding via custom initializer; allows auto-conformance to `Decodable`` and per-property opt-out.
- [ObfuscateMacro](https://github.com/p-x9/ObfuscateMacro): A macro for obfuscating strings and make them harder to find by binary analysis.
- [MemoizeMacro](https://github.com/tornikegomareli/MemoizeMacro?tab=readme-ov-file): A macro for effortless function memoization in Swift
- [MemberwiseInit](https://github.com/gohanlon/swift-memberwise-init-macro): Informed by explicit developer cues, `@MemberwiseInit` can more often automatically provide your intended memberwise init, while following the same safe-by-default semantics underlying Swift’s memberwise initializers.
- [PropertyTracer](https://github.com/p-x9/swift-property-tracer): Library for tracing access to properties.`@PropertyTraced` macro makes possible to trace from which method a property has been accessed.
- [Swift Macros](https://github.com/bernndr/swift-macros): Contains a collection of useful macros:
  - `#symbol`: Verify if SFSymbol is valid
  - `#URL`: Validate and return URL Object
  - `#unwrap`: Unwrap value.
  - `@AssociatedValues`: Add variables to retrieve the associated values.
  - `@Singleton`: Generate singleton code for struct and class.
  - More to come...
- [Migrator](https://github.com/narek-sv/Migrator): Migrator is a versatile Swift package designed to streamline the execution of asynchronous tasks with dependency management on all Apple platforms. The package also includes a handy macro for semantic versioning ([SemVer 2.0.0](https://semver.org/)).
  - `#SemanticVersion("1.2.3")`
- [Equatable](https://github.com/spacenation/swift-equatable): A macro for synthesizing `Equatable` conformance for classes and actors.
- [CloakedString](https://github.com/pykaso/swiftmacro-cloaked-string): A macro designed to improve the security of open text strings in Swift applications
- [SmartLogMacro](https://github.com/AndriyGo/SmartLogMacro): Powerful Swift macros for structured logging, privacy, and seamless 3rd-party log forwarding



---

_**Take part in this exciting evolution in Swift. Your contributions are most welcome!**_

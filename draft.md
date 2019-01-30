# Coding guidelines

## Table of contents

1. Preface
    - DO NOT follow blindly theses advices, they should be adapted to the context (team, project, legacy...)
1. General rules
    - code comments MUST explain the WHY, not the HOW (implementation) or the WHAT (types)
    - use short names in small context and more descriptive ones in larger contexts
1. Language rules
    - DO NOT throw exceptions or functions that throw (use Try)
    - DO NOT use null (use Option)
    - DO NOT use return
    - DO NOT use Unit (create a Done case object and use it instead)
    - DO NOT abuse of primitive types (String, Int, Boolean, Seq, Map, Option...)
    - DO NOT use little typed types (such as Any, AnyRef, Config, JsValue, Map[String, String]...)
    - PREFER using immutable structures over mutable ones
    - MUST explicitly write type for every function or public attribute
    - MUST use pure functions (as much as possible)
    - MUST define constraints in types (NonEmptyList, PositiveInt, class with validation in builder)
    - case classes MUST be final
    - sealed trait MUST extends Product with Serializable
    - DO NOT use mutable state
    - PREFER NOT using lazy val
    - DO NOT use implicit functions (except for type classes)
1. Code architecture
    - MUST split technical and business code
    - DO NOT build invalid objects
    - DO NOT rely on temporal coupling
1. Performance
    - DO NOT discuss about performance without a benchmark highlighting the problem
1. Syntax rules
    - Functions SHOULD have less than 20 lines, less than 10 is better and more than 50 is not acceptable
    - Lines SHOULD be less than 120 chars and more than 160 is not acceptable
    - Use 2 spaces for indentation
    - Add an empty line at the end of each file

## Interesting tools

- scalafmt
- scalastyle

## References and inspirations

- [Alexandru Nedelcu best practices](https://github.com/alexandru/scala-best-practices)
- [Nicolas Rinaudo best practices](https://nrinaudo.github.io/scala-best-practices/)
- Li Haoyi's Strategic Scala Style: [Principle of Least Power](http://www.lihaoyi.com/post/StrategicScalaStylePrincipleofLeastPower.html) [Conciseness & Names](http://www.lihaoyi.com/post/StrategicScalaStyleConcisenessNames.html) [Practical Type Safety](http://www.lihaoyi.com/post/StrategicScalaStylePracticalTypeSafety.html) [Designing Datatypes](http://www.lihaoyi.com/post/StrategicScalaStyleDesigningDatatypes.html)
- Jakub Kozłowski talk: [7* sins of a Scala beginner](https://kubukoz.github.io/talks/seven-sins-of-a-scala-developer/slides) ([vidéo](https://www.youtube.com/watch?v=Z2YzCzfUNNk))
- Nicolas Rinaudo talk: [Scala Best Practices I Wish Someone'd Told Me About](https://nrinaudo.github.io/talk-scala-best-practices) ([vidéo](https://www.youtube.com/watch?v=lvlnH-uEjZA))
- [Knoldus best practices](https://blog.knoldus.com/scala-best-practices)
- [Databricks best practices](https://github.com/databricks/scala-style-guide)
- [PayPal best practices](https://github.com/paypal/scala-style-guide)
- [Twitter best practices](http://twitter.github.io/effectivescala)

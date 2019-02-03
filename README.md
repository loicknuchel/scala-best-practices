# Scala Best Practices by Loïc Knuchel
(meaning their are my personal ones, not community ones)

I believe there is 3 very different groups in the Scala community:
- **OOP puristes**: coming from OOP languages and use Scala as a better OOP language
- **FP minimalists**: sold to FP but want to keep code
- **FP purists**:

Codes used in this guide:
- [MUST] is for rules that should be transgressed only in last resort and needs an explanation of why in comment next to it
- [PREFER] is for rules that should be followed in most cases but can be sometimes transgressed for more practical code
- **Rules in bold** are the important ones I consider you essential to any Scala code

## Table of contents

1. Preface
    - [MUST] Do not take theses rules as is, you should understand and adapt them to your context
1. General
    - [PREFER] Code comments should explain WHY the code has been done this way, not HOW it does it
    - [MUST] Names should be meaningful
1. Language
1. FP
    - [MUST] Functions should be total
    - [PREFER] Functions should be pure
1. Architecture
    - **[MUST] Split technical and business code**
    - **[[MUST] Encode business rules in types as much as possible](guidelines/artchitecture/encode-business-rules-in-types-as-much-as-possible.md)**
    - [MUST] Avoid building invalid objects
    - [MUST] Avoid temporal coupling
1. Performance
    - [MUST] Performance should not be discussed without a benchmark highlighting the problem and the metrics that must be reached
1. Play framework
1. Syntax
    - [PREFER] Functions should have less than 20 lines, less than 10 is better, more than 50 is not acceptable
    - [PREFER] Lines should be less than 120 chars, more than 160 is not acceptable
    - [PREFER] Indentation should use 2 spaces
    - [PREFER] Each file should be terminated by an empty line

## Interesting tools

- scalafmt
- scalastyle
- wartRemover

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

## Contribute

Open a PR or an Issue and let's discuss

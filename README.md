# Scalazzi

[![Join the chat at https://gitter.im/scalaz/scalazzi](https://badges.gitter.im/scalaz/scalazzi.svg)](https://gitter.im/scalaz/scalazzi?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This project is configuration to enforce the [scalazzi](http://yowconference.com.au/slides/yowwest2014/Morris-ParametricityTypesDocumentationCodeReadability.pdf) safe subset of scala with [scalafix](https://scalacenter.github.io/scalafix/docs/users/installation).

To install, first install scalafix, e.g. in `project/plugins.sbt`

```scala
addSbtPlugin("ch.epfl.scala" % "sbt-scalafix" % "0.6.0-M12")
```

and enable the compiler plugin for each project in `build.sbt`

```scala
scalacOptions += "-Yrangepos"
addCompilerPlugin(scalafixSemanticdb)
```

If anything goes wrong, ask on the [scalacenter/scalafix](https://gitter.im/scalacenter/scalafix) channel.

Then copy the `scalafix.conf` from here to `.scalafix.conf` in your project root and run `scalafix` in your sbt shell ([read the manual](https://scalacenter.github.io/scalafix/docs/users/installation) to learn more).

As an added bonus, you are also now set up to beta test [Metals](https://github.com/scalameta/metals) and [Metadoc](https://github.com/scalameta/metadoc).

If you would like to contribute to this initiative you can:

- pick up the tickets in this repo to ease installation and extensibility
- [expand the list of manually verified "safe" methods](CONTRIBUTING.md)
- [implement and improve scalazzi rules inside scalafix](https://github.com/scalacenter/scalafix/issues?q=is%3Aissue+is%3Aopen+label%3Ascalazzi)

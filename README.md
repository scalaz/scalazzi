# Scalazzi

This project is configuration to enforce the [scalazzi](http://yowconference.com.au/slides/yowwest2014/Morris-ParametricityTypesDocumentationCodeReadability.pdf) safe subset of scala with [scalafix](https://scalacenter.github.io/scalafix/docs/users/installation).

To install, first install scalafix, e.g. in `project/plugins.sbt`

```scala
addSbtPlugin("ch.epfl.scala" % "sbt-scalafix" % "0.6.0-M12")
```

and copy the `scalafix.conf` from here to `.scalafix.conf` in your project root.

If you would like to contribute to this initiative you can:

- pick up the tickets in this repo to ease installation and extensibility
- [expand the list of manually verified "safe" methods](CONTRIBUTING.md)
- [implement and improve scalazzi rules inside scalafix](https://github.com/scalacenter/scalafix/issues?q=is%3Aissue+is%3Aopen+label%3Ascalazzi)

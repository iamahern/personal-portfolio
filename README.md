# Personal Portolio
Description of OpenSource and Major Academic Projects

Index:
* GitHub projects
  * [IfInjector](#ifinjector) - C# dependency injection framework
  * [Runas User Credential Access Jenkins Plugin](#runas-user-credential-access-jenkins-plugin)
* Boring but critical open source patching
  * [Patching Xerces on the Internet](#patching-xerces)
* [Academic (GATech)](gatech/README.md)
  * [Computational Photography](gatech/computational_photography/README.md)
  * [Reinforcement Learning](gatech/reinforcement_learning/README.md)


# Work/Personal Projects

## IFInjector

GitHub [IfInjector](https://github.com/iamahern/IfInjector)

This was a personal project resulting from a decision to learn C# to gain an understanding of the language features available there (vs. Java). While doing so, I experimented with frameworks for developing cross platform mobile applications using C#. At the time, I found options for "mobile capable" dependency injection frameworks lacking and decided to write my own. As part of this, I took the opportunity to learn the LINQ framework which provides a means to compile expressions into byte-code (on non-mobile platforms).

The project originally started as a fork of the fFastInjector framework, but was eventually rewritten for performance. For a brief few days the framework was near the top of some of the C# dependency injection framework benchmarks. You can find some references to the project on the internet archive:
https://web.archive.org/web/20180611033508/https://github.com/danielpalme/IocPerformance

The projet was just for fun and demonstrates an antipattern of writing ones own framework for X when functional Open Source alternatives exist.


## Runas User Credential Access Jenkins Plugin

GitHub [Runas User Credential Access Jenkins Plugin](https://github.com/iamahern/runas-user-credential-access-project)

This plugin saw years of service within Watson Health as part of a ["MacGyvered"](https://www.merriam-webster.com/words-at-play/what-does-macgyver-mean-slang-definition), Home Grown GitOps solution. The overall problem was to lift and shift a legacy VM / runbook heavy set of process to IBM Cloud / Kubernetes. Complicating the problem the senior architect would not allow the use of Terraform or any Dev Ops tool which required a server / maintanence effort.

This plugin allows for user private credentials to be accessed by specially authorized Jenkins jobs without a user needing to select them explicitly in a drop down. One constraint of Jenkins is that private credentials cannot be forwarded to chained jobs. By allowing this propagation, the plugin allowed for chaining of automation jobs utilizing a user's personal credentials. All cloud operations were thus executed with a user's personal API key and GitHub / config changes using a personal access token. In both cases, this results in both an audit of the user carrying out the admin operation as well as the git / config change operations. Revoking the user from either the production git config repository OR the production cloud account resulted in the user being unable to perform production changes via Jenkins.


# Boring but Critical

A lot of being a good Open Source citzen is contributing / reporting issues when you see them as well as chasing Open Source maintainers (occassionally) to patch / fix their software. Below is a highlight of this work.


## Patching Xerces

In 2018 Xerces released the XercesImpl 2.12.0 patch for a Denile of Service attack discovered in late 2017. Although a patch was released on the Xerces homepage, the project maintainers failed to upload a patch to Maven Central. As a result a number of downstream projects continued to ship with the vulnerability.

After  [discussions](https://github.com/gradle/gradle/issues/5598) with the Gradle maintainers, I joined the Xerces mailing lists / [weighed in on some defects](https://issues.apache.org/jira/browse/XERCESJ-1695) and eventually ~annoyed~ persueded the maintainer to upload a patch. [Gradle](https://github.com/gradle/gradle/issues/5724) and probably dozens of other open source projects were patched as a result.
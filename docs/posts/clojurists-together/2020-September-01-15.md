---
title: Practicalli Project Update 2
date: 2020-09-15
authors:
  - practicalli
categories:
  - clojurists-together
---

![Clojurists Together Logo](https://raw.githubusercontent.com/practicalli/graphic-design/live/buttons/practicalli-clojurists-together-button.svg){align=right loading=lazy style="height:150px;width:150px"}

Invested time to understand the changes coming to the Clojure CLI tools and understand the opportunities that [Clojure exec](https://insideclojure.org/2020/09/04/clj-exec/) (`:exec-fn` & `:exec-args`) brings to aliases. These changes provided a catalyst to start redesigning the aliases used in [practicalli/clojure-cli-config](https://practical.li/clojure/clojure-spec/data/defining-specifications/#naming-fully-qualified-keywords).

<!-- more -->

## Practicalli Study Group
Continuing the Banking on Clojure project, especially around database access.  The database schema was refined along with improved approaches to creating database schema, using transactional updates and ensuring connections are closed.  The next.jdbc friendly functions were explored and a CRUD approach implemented.

- [:fontawesome-brands-youtube: 082 - Banking On Clojure - Part3 - next.jdbc for SQL in Clojure](https://youtu.be/sBdmwDUp1Ho)
- [:fontawesome-brands-youtube: 083 - Banking On Clojure - Part4 - Updating data in the database](https://youtu.be/DmYlNTe7Gds)

Next steps will be to use Clojure spec for generative testing with the database, add connection pooling and using lifecycle management libraries.


## Practicalli WebApps
Updated sections on [H2 Database](https://practical.li/clojure-web-services/relational-databases-and-sql/h2-database/) and Banking on Clojure

- [Design and Create Database Tables](https://practical.li/clojure-web-services/projects/banking-on-clojure/database-tables/)
- [Defining Database Queries - different approaches](https://practical.li/clojure-web-services/projects/banking-on-clojure/database-queries/)
- [Create database records](https://practical.li/clojure-web-services/projects/banking-on-clojure/create-records/)
- [Read Database Records](https://practical.li/clojure-web-services/projects/banking-on-clojure/read-records/)
- [Update Records in the database](https://practical.li/clojure-web-services/projects/banking-on-clojure/update-records/)
- [Delete Records in the database](https://practical.li/clojure-web-services/projects/banking-on-clojure/delete-records/)


## Practicalli Clojure

Added [core principles for writing effective unit tests](https://practical.li/clojure/testing/unit-testing/) in Clojure. Included project configuration examples of unit tests for Leiningen and Clojure CLI tools.

Included example configuration for Emacs CIDER test runner and link to the test runner configurations in [practicalli/clojure-cli-config](https://github.com/practicalli/clojure-cli-config/?tab=readme-ov-file#unit-testing-frameworks).


## Clojure CLI Config

Created a draft guide to changes in the next release of the Clojue CLI tools, to understand the significance of the changes it introduces.  The `-X` flag for executing a function with EDN arguments (hash-map arguments) has already been introduced and the new release depreciates the generic `-A` alias in favor of `-M`.  In the long term using the `-X` flag with functions that take a structured argument looks to be an excellent approach.

Started a redesign of practicalli/clojure-cli-config using qualified keywords for alias names.  The Library repositories keyword, `:mvn/repos`, is already qualified, so this redesign brings the aliases in line with that style.  The alias keywords are prepended with names to communicate the category of purpose for each alias, e.g. repl, project, env, lib, inspect, build, deploy.

As part of the redesign, the new flags introduced with Clojure CLI tools, `-M` and `-X`, are used.  The `-X` flag is the preferred Clojure command line flag to use for the aliases, where the library supports executing a function from the library that takes a hash-map of arguments.  Otherwise `-M` flag replaces `-A` flag and continues to use `clojure.main` to call the `-main` function of the given main namespace.

Add project/check to give detailed report on compilation issues for a project

UPDATE: all aliases in [Practicalli CLI Config](https://github.com/practicalli/clojure-cli-config) use fully qualified names.

## Practicalli Spacemacs

Resolved simple bug fixes raised by the community.

---
Thank you.

[:globe_with_meridians: Practical.li Website](https://practical.li){target=_blank .md-button}

[:fontawesome-brands-github: Practical.li GitHub Org](https://github.com/practicalli){target=_blank .md-button}
[:fontawesome-brands-github: practicalli-johnny profile](https://github.com/practicalli-johnny){target=_blank .md-button}

[:fontawesome-brands-mastodon: @practicalli@clj.social](https://clj.social/@practicalli){target=_blank .md-button}
[:fontawesome-brands-twitter: @practical_li](https://twitter.com/practcial_li){target=_blank .md-button}

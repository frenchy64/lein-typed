# lein-typed

Type checking for Clojure with Clojure core.typed.

## Usage

Use this for user-level plugins:

Put `[lein-typed "0.1.0"]` into the `:plugins` vector of your
`:user` profile, or if you are on Leiningen 1.x do `lein plugin install
lein-typed 0.1.0`.

Use this for project-level plugins:

Put `[lein-typed "0.1.0"]` into the `:plugins` vector of your project.clj.

To type check many namespaces, add namespaces to your project.clj like

    :core.typed {:check [my.ns1 my.ns2]}

Then run

    $ lein typed check 

To type check a namespace, provide a namespace symbol to check-ns:

    $ lein typed check-ns typed-demo.core
    Initializing core.typed ...
    "Elapsed time: 5705.247176 msecs"
    core.typed initialized.
    Start collecting typed-demo.core
    Finished collecting typed-demo.core
    Collected 1 namespaces in 6039.963178 msecs
    Start checking typed-demo.core
    Checked typed-demo.core in 94.891391 msecs
    Checked 1 namespaces (approx. 7 lines) in 6138.087383 msecs

## License

Copyright © 2013 Ambrose Bonnaire-Sergeant

Distributed under the Eclipse Public License, the same as Clojure.
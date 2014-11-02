# keybase-clj

[ ![Codeship Status for niftyn8/keybase-clj](https://www.codeship.io/projects/88f64b70-4519-0132-64da-460c6dc64c0a/status)](https://www.codeship.io/projects/44937)

A Clojure library for interacting with the keybase.io API **NOTE:** This totally doesn't work yet...

## Usage

```
(ns coolapp.core
  (:require [keybase.io.client :as keybase])
  (:gen-class :main true))

(def auth [signed-message]
  (keybase/auth signed-message))

(defn encrypt [msg token]
  (with_auth token (keybase/encrypt msg)))

(defn -main [signed-message message]
  (let [token (auth auth "signed message")]
    (println (encrypt message token))))
```
## License

Copyright © 2014 FIXME

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.

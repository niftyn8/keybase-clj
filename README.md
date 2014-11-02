# keybase-clj

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

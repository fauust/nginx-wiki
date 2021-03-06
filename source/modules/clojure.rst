
.. meta::
   :description: The Clojure module is used for embedding Clojure programs.

Clojure
=======

`Nginx-Clojure <http://nginx-clojure.github.io>`_ is a NGINX module for embedding Clojure or Java or Groovy programs, typically those Ring based handlers.

There are some core features:

#. Compatible with Ring and obviously supports those Ring based frameworks, such as Compojure etc.
#. Use Clojure / Java / Groovy to write simple ring handlers for http services.
#. Use Clojure / Java / Groovy to write a simple NGINX rewrite handler to set var or return errors before proxy pass or content ring handler.
#. Non-blocking coroutine based socket which is Compatible with Java Socket API and works well with largely existing java library such as apache http client, mysql jdbc drivers. With this feature one java main thread can handle thousands of connections.
#. Handle multiple sockets parallel in sub coroutines, e.g. we can invoke two remote services at the same time.
#. Asynchronous callback API of socket for some advanced usage.
#. Run initialization clojure code when NGINX worker starting.
#. Support user defined http request method.
#. Compatible with the NGINX lastest stable version 1.6.0. (NGINX 1.4.x is also ok, older version is not tested and maybe works).
#. One of benifits of NGINX is worker processes are automatically restarted by a master process if they crash.
#. Utilizes lazy headers and direct memory operation between NGINX and JVM to fast handle dynamic contents from Clojure or Java code.
#. Utilizes NGINX zero copy file sending mechanism to fast handle static contents controlled by Clojure or Java code.
#. Supports Linux x64, Linux x86 32bit, Win32 and Mac OS X. Win64 users can also run it with a 32bit JRE/JDK.

By the way, it is very fast. The benchmarks can be found :github:`here <ptaoussanis/clojure-web-server-benchmarks>`

Please visit `nginx-clojure.github.io <http://nginx-clojure.github.io>`_ for more details.

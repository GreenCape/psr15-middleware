# PSR-15 HTTP Server Middleware Components

This is a curated (most likely not complete) list of **[PSR-15](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-15-request-handlers.md) HTTP Server Middleware Components**.
 
### Authentication

* [Tuupola](https://github.com/tuupola)/**[BrancaAuthentication](https://github.com/tuupola/branca-middleware)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/tuupola/branca-middleware.svg?style=plastic)](https://packagist.org/packages/tuupola/branca-middleware)
    ![GitHub last commit](https://img.shields.io/github/last-commit/tuupola/branca-middleware.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/tuupola/branca-middleware.svg?style=plastic)<br>
    Implements [Branca token](https://github.com/tuupola/branca-spec) authentication. Branca is similar to JWT but more secure and has smaller token size.
    Does **not** implement OAuth authorization server nor does it provide ways to generate, issue or store the authentication tokens.
    Only parses and authenticates a token when passed via header or cookie.
* [Middlewares](https://github.com/middlewares)/**[HttpAuthentication](https://github.com/middlewares/http-authentication)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/http-authentication.svg?style=plastic)](https://packagist.org/packages/middlewares/http-authentication)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/http-authentication.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/http-authentication.svg?style=plastic)<br>
    Implements [RFC 2617 Http Authentication](https://tools.ietf.org/html/rfc2617). Contains the following components:
  * [Middlewares](https://github.com/middlewares)/**[BasicAuthentication](https://github.com/middlewares/http-authentication#basicauthentication)**
  * [Middlewares](https://github.com/middlewares)/**[DigestAuthentication](https://github.com/middlewares/http-authentication#digestauthentication)**
* [Tuupola](https://github.com/tuupola)/**[HttpBasicAuthentication](https://github.com/tuupola/slim-basic-auth)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/tuupola/slim-basic-auth.svg?style=plastic)](https://packagist.org/packages/tuupola/slim-basic-auth)
    ![GitHub last commit](https://img.shields.io/github/last-commit/tuupola/slim-basic-auth.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/tuupola/slim-basic-auth.svg?style=plastic)<br>
    Implements [HTTP Basic Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication). Supports different authenticators.
* [Tuupola](https://github.com/tuupola)/**[JwtAuthentication](https://github.com/tuupola/slim-jwt-auth)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/tuupola/slim-jwt-auth.svg?style=plastic)](https://packagist.org/packages/tuupola/slim-jwt-auth)
    ![GitHub last commit](https://img.shields.io/github/last-commit/tuupola/slim-jwt-auth.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/tuupola/slim-jwt-auth.svg?style=plastic)<br>
    Implements JSON Web Token Authentication.
    Does not implement OAuth 2.0 authorization server nor does it provide ways to generate, issue or store authentication tokens.
    Only parses and authenticates a token when passed via header or cookie.

### Cache

* [Middlewares](https://github.com/middlewares)/**[Cache](https://github.com/middlewares/cache)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/cache.svg?style=plastic)](https://packagist.org/packages/middlewares/cache)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/cache.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/cache.svg?style=plastic)<br>
    Adds cache support.
  * [Middlewares](https://github.com/middlewares)/**[Cache](https://github.com/middlewares/cache#cache)**<br>
  Saves the response headers in a [PSR-6 cache pool](http://www.php-fig.org/psr/psr-6/) and returns `304 Not modified` responses if the response is still valid.
  * [Middlewares](https://github.com/middlewares)/**[CachePrevention](https://github.com/middlewares/cache#cacheprevention)**<br>
  Adds response headers for cache prevention. Useful in development environments.
  * [Middlewares](https://github.com/middlewares)/**[Expires](https://github.com/middlewares/cache#expires)**<br>
  Adds the `Expires` and `Cache-Control: max-age` headers to the response.
* [Middlewares](https://github.com/middlewares)/**[Filesystem](https://github.com/middlewares/filesystem)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/filesystem.svg?style=plastic)](https://packagist.org/packages/middlewares/filesystem)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/filesystem.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/filesystem.svg?style=plastic)<br>
    Saves or reads responses from files. It uses [Flysystem](http://flysystem.thephpleague.com/) as filesystem handler, so you can use not only local directories, but also any other adapter like [FTP](http://flysystem.thephpleague.com/adapter/ftp/), [SFTP](http://flysystem.thephpleague.com/adapter/sftp/), [Dropbox](http://flysystem.thephpleague.com/adapter/dropbox/), etc. Contains the following components:
  * [Middlewares](https://github.com/middlewares)/**[Reader](https://github.com/middlewares/filesystem#reader)**
  * [Middlewares](https://github.com/middlewares)/**[Writer](https://github.com/middlewares/filesystem#writer)**

### Client Info

* [Middlewares](https://github.com/middlewares)/**[ClientIp](https://github.com/middlewares/client-ip)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/client-ip.svg?style=plastic)](https://packagist.org/packages/middlewares/client-ip)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/client-ip.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/client-ip.svg?style=plastic)<br>
    Detects the client IP and saves it as a request attribute.
* [Middlewares](https://github.com/middlewares)/**[Geolocation](https://github.com/middlewares/geolocation)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/geolocation.svg?style=plastic)](https://packagist.org/packages/middlewares/geolocation)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/geolocation.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/geolocation.svg?style=plastic)<br>
    Determines the client's geo location using the IP address and [Geocoder](https://github.com/geocoder-php/Geocoder) and saves the result as a request attribute.
* [Middlewares](https://github.com/middlewares)/**[Negotiation](https://github.com/middlewares/negotiation)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/negotiation.svg?style=plastic)](https://packagist.org/packages/middlewares/negotiation)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/negotiation.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/negotiation.svg?style=plastic)<br>
    Implements content negotiation using [wildurand/Negotiation](https://github.com/willdurand/Negotiation). Contains the following components:
  * [Middlewares](https://github.com/middlewares)/**[ContentType](https://github.com/middlewares/negotiation#contenttype)**
  * [Middlewares](https://github.com/middlewares)/**[ContentLanguage](https://github.com/middlewares/negotiation#contentlanguage)**
  * [Middlewares](https://github.com/middlewares)/**[ContentEncoding](https://github.com/middlewares/negotiation#contentencoding)**

### Compression

* [Middlewares](https://github.com/middlewares)/**[Encoder](https://github.com/middlewares/encoder)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/encoder.svg?style=plastic)](https://packagist.org/packages/middlewares/encoder)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/encoder.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/encoder.svg?style=plastic)<br>
    Encodes the response body with `gzip` or `deflate` if the `Accept-Encoding` header is present and adds the `Content-Encoding` header. Contains the following components:
  * [Middlewares](https://github.com/middlewares)/**[DeflateEncoder](https://github.com/middlewares/encoder#deflateencoder)**
  * [Middlewares](https://github.com/middlewares)/**[GzipEncoder](https://github.com/middlewares/encoder#gzipencoder)**
* [Middlewares](https://github.com/middlewares)/**[Minifier](https://github.com/middlewares/minifier)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/minifier.svg?style=plastic)](https://packagist.org/packages/middlewares/minifier)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/minifier.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/minifier.svg?style=plastic)<br>
    Minifies HTML, CSS and Javascript content using [mrclay/minify](https://github.com/mrclay/minify). Contains the following components:
  * [Middlewares](https://github.com/middlewares)/**[CssMinifier](https://github.com/middlewares/minifier#cssminifier)**
  * [Middlewares](https://github.com/middlewares)/**[HtmlMinifier](https://github.com/middlewares/minifier#htmlminifier)**
  * [Middlewares](https://github.com/middlewares)/**[JsMinifier](https://github.com/middlewares/minifier#jsminifier)**

### Development Utilities

* [Middlewares](https://github.com/middlewares)/**[Debugbar](https://github.com/middlewares/debugbar)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/debugbar.svg?style=plastic)](https://packagist.org/packages/middlewares/debugbar)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/debugbar.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/debugbar.svg?style=plastic)<br>
    Inserts [PHP DebugBar](http://phpdebugbar.com) automatically in HTML responses.
* [PhpMiddleware](https://github.com/php-middleware) / **[Debugbar](https://github.com/php-middleware/phpdebugbar)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/php-middleware/php-debug-bar.svg?style=plastic)](https://packagist.org/packages/php-middleware/php-debug-bar)
    ![GitHub last commit](https://img.shields.io/github/last-commit/php-middleware/phpdebugbar.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/php-middleware/php-debug-bar.svg?style=plastic)<br>
    Inserts [PHP DebugBar](http://phpdebugbar.com) automatically in HTML responses.
* [PhpMiddleware](https://github.com/php-middleware) / **[Maintenance](https://github.com/php-middleware/maintenance)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/php-middleware/maintenance.svg?style=plastic)](https://packagist.org/packages/php-middleware/maintenance)
    ![GitHub last commit](https://img.shields.io/github/last-commit/php-middleware/maintenance.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/php-middleware/maintenance.svg?style=plastic)<br>
    Displays a `503` maintenance page according to  [How to deal with planned site downtime](http://googlewebmastercentral.blogspot.com/2011/01/how-to-deal-with-planned-site-downtime.html) in the Google Webmaster Central Blog.
* [PhpMiddleware](https://github.com/php-middleware) / **[RequestId](https://github.com/php-middleware/request-id)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/php-middleware/request-id.svg?style=plastic)](https://packagist.org/packages/php-middleware/request-id)
    ![GitHub last commit](https://img.shields.io/github/last-commit/php-middleware/request-id.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/php-middleware/request-id.svg?style=plastic)<br>
    Generates a request id (correlation id) and adds it to the header of request and response. Supports several id generators.
* [PhpMiddleware](https://github.com/php-middleware) / **[RequestSimulator](https://github.com/php-middleware/request-simulator)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/php-middleware/request-simulator.svg?style=plastic)](https://packagist.org/packages/php-middleware/request-simulator)
    ![GitHub last commit](https://img.shields.io/github/last-commit/php-middleware/request-simulator.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/php-middleware/request-simulator.svg?style=plastic)<br>
    Provides a form for handcrafted requests. Useful for debugging and testing.
* [Middlewares](https://github.com/middlewares)/**[ResponseTime](https://github.com/middlewares/response-time)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/response-time.svg?style=plastic)](https://packagist.org/packages/middlewares/response-time)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/response-time.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/response-time.svg?style=plastic)<br>
    Calculates the response time (in miliseconds) and saves it into the `X-Response-Time` header.
* [Tuupola](https://github.com/tuupola)/**[ServerTiming](https://github.com/tuupola/server-timing-middleware)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/tuupola/server-timing-middleware.svg?style=plastic)](https://packagist.org/packages/tuupola/server-timing-middleware)
    ![GitHub last commit](https://img.shields.io/github/last-commit/tuupola/server-timing-middleware.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/tuupola/server-timing-middleware.svg?style=plastic)<br>
    Implements the [Server-Timing](http://wicg.github.io/server-timing/) header which can be used for displaying server side timing information on Chrome DevTools.
* [Middlewares](https://github.com/middlewares)/**[Shutdown](https://github.com/middlewares/shutdown)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/shutdown.svg?style=plastic)](https://packagist.org/packages/middlewares/shutdown)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/shutdown.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/shutdown.svg?style=plastic)<br>
    Displays a `503` maintenance page.
* [Middlewares](https://github.com/middlewares)/**[Uuid](https://github.com/middlewares/uuid)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/uuid.svg?style=plastic)](https://packagist.org/packages/middlewares/uuid)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/uuid.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/uuid.svg?style=plastic)<br>
    Generates a [RFC 4122](http://tools.ietf.org/html/rfc4122) version 4 compatible UUID (Universally Unique Identifier) using [ramsey/uuid](https://github.com/ramsey/uuid) and saves it in the `X-Uuid` header of the request and the response. Useful for debugging purposes.

### Error / Exception Handling

* [Middlewares](https://github.com/middlewares)/**[ErrorHandler](https://github.com/middlewares/error-handler)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/error-handler.svg?style=plastic)](https://packagist.org/packages/middlewares/error-handler)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/error-handler.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/error-handler.svg?style=plastic)<br>
    Executes a handler if the response returned by subsequent middleware has any error (status code `400`-`599`) or a `Middlewares\HttpErrorException` is thrown.
* [Middlewares](https://github.com/middlewares)/**[Whoops](https://github.com/middlewares/whoops)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/whoops.svg?style=plastic)](https://packagist.org/packages/middlewares/whoops)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/whoops.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/whoops.svg?style=plastic)<br>
    Uses [Whoops](https://github.com/filp/whoops) as error handler.

### Logging

* [Middlewares](https://github.com/middlewares)/**[AccessLog](https://github.com/middlewares/access-log)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/access-log.svg?style=plastic)](https://packagist.org/packages/middlewares/access-log)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/access-log.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/access-log.svg?style=plastic)<br>
    Generates access logs for each request using [Apache's access log format](https://httpd.apache.org/docs/2.4/logs.html#accesslog). Requires a [PSR-3 log implementation](https://packagist.org/providers/psr/log-implementation).
* [PhpMiddleware](https://github.com/php-middleware) / **[LogExceptions](https://github.com/php-middleware/log-exceptions)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/php-middleware/log-exceptions.svg?style=plastic)](https://packagist.org/packages/php-middleware/log-exceptions)
    ![GitHub last commit](https://img.shields.io/github/last-commit/php-middleware/log-exceptions.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/php-middleware/log-exceptions.svg?style=plastic)<br>
    Logs and rethrows all (unhandled) exceptions to a [PSR-3 log implementation](https://packagist.org/providers/psr/log-implementation).
* [PhpMiddleware](https://github.com/php-middleware) / **[LogHttpMessages](https://github.com/php-middleware/log-http-messages)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/php-middleware/log-http-messages.svg?style=plastic)](https://packagist.org/packages/php-middleware/log-http-messages)
    ![GitHub last commit](https://img.shields.io/github/last-commit/php-middleware/log-http-messages.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/php-middleware/log-http-messages.svg?style=plastic)<br>
    Provides logging of request and response messages to a [PSR-3 log implementation](https://packagist.org/providers/psr/log-implementation).

### Proxy

* [Middlewares](https://github.com/middlewares)/**[Proxy](https://github.com/middlewares/proxy)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/proxy.svg?style=plastic)](https://packagist.org/packages/middlewares/proxy)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/proxy.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/proxy.svg?style=plastic)<br>
    Creates an HTTP proxy using [Guzzle](https://github.com/guzzle/guzzle).
* [Ellipse](https://github.com/ellipsephp)/**[ScopedMiddleware](https://github.com/ellipsephp/middleware-scoped)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/ellipsephp/middleware-scoped.svg?style=plastic)](https://packagist.org/packages/ellipsephp/middleware-scoped)
    ![GitHub last commit](https://img.shields.io/github/last-commit/ellipsephp/middleware-scoped.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/ellipsephp/middleware-scoped.svg?style=plastic)<br>
    Proxies other middleware based on URL condition. Contains the following components: 
  * [Ellipse](https://github.com/ellipsephp)/**[BasepathBasedMiddleware](https://github.com/ellipsephp/middleware-scoped)**<br>
  * [Ellipse](https://github.com/ellipsephp)/**[HostBasedMiddleware](https://github.com/ellipsephp/middleware-scoped)**<br>
  * [Ellipse](https://github.com/ellipsephp)/**[SchemeBasedMiddleware](https://github.com/ellipsephp/middleware-scoped)**<br>
  * [Ellipse](https://github.com/ellipsephp)/**[UrlPartBasedMiddleware](https://github.com/ellipsephp/middleware-scoped)**<br>

### Robots

* [PhpMiddleware](https://github.com/php-middleware) / **[BlockRobots](https://github.com/php-middleware/block-robots)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/php-middleware/block-robots.svg?style=plastic)](https://packagist.org/packages/php-middleware/block-robots)
    ![GitHub last commit](https://img.shields.io/github/last-commit/php-middleware/block-robots.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/php-middleware/block-robots.svg?style=plastic)<br>
    Enables/disables the robots of the search engines for non-production environment. Automatically adds the `X-Robots-Tag` header in all responses and returns a default body for `/robots.txt` request.
* [Middlewares](https://github.com/middlewares)/**[Recaptcha](https://github.com/middlewares/recaptcha)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/recaptcha.svg?style=plastic)](https://packagist.org/packages/middlewares/recaptcha)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/recaptcha.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/recaptcha.svg?style=plastic)<br>
     Uses [Google reCAPTCHA](https://github.com/google/recaptcha) library for spam prevention. Returns a `403` response if the request is not valid.
* [Middlewares](https://github.com/middlewares)/**[Robots](https://github.com/middlewares/robots)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/robots.svg?style=plastic)](https://packagist.org/packages/middlewares/robots)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/robots.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/robots.svg?style=plastic)<br>
    Enables/disables the robots of the search engines for non-production environment. Automatically adds the `X-Robots-Tag` header in all responses and returns a default body for `/robots.txt` request.

### Router

* [Middlewares](https://github.com/middlewares)/**[AuraRouter](https://github.com/middlewares/aura-router)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/aura-router.svg?style=plastic)](https://packagist.org/packages/middlewares/aura-router)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/aura-router.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/aura-router.svg?style=plastic)<br>
    Uses [Aura.Router](https://github.com/auraphp/Aura.Router/) and stores the route handler in a request attribute.
* [Middlewares](https://github.com/middlewares)/**[FastRoute](https://github.com/middlewares/fast-route)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/fast-route.svg?style=plastic)](https://packagist.org/packages/middlewares/fast-route)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/fast-route.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/fast-route.svg?style=plastic)<br>
    Uses [FastRoute](https://github.com/nikic/FastRoute) for handler discovery.
* [Middlewares](https://github.com/middlewares)/**[RequestHandler](https://github.com/middlewares/request-handler)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/request-handler.svg?style=plastic)](https://packagist.org/packages/middlewares/request-handler)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/request-handler.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/request-handler.svg?style=plastic)<br>
    Executes request handlers discovered by a router.
* [Ellipse](https://github.com/ellipsephp)/**[Router](https://github.com/ellipsephp/router-adapter)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/ellipsephp/router-adapter.svg?style=plastic)](https://packagist.org/packages/ellipsephp/router-adapter)
    ![GitHub last commit](https://img.shields.io/github/last-commit/ellipsephp/router-adapter.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/ellipsephp/router-adapter.svg?style=plastic)<br>
    Provides different routers. Supported are:
  * [Ellipse](https://github.com/ellipsephp)/**[AuraRouter](https://github.com/ellipsephp/router-aura)**
      [![Latest Version on Packagist](https://img.shields.io/packagist/v/ellipsephp/router-aura.svg?style=plastic)](https://packagist.org/packages/ellipsephp/router-aura)
      ![GitHub last commit](https://img.shields.io/github/last-commit/ellipsephp/router-aura.svg?style=plastic)
      ![License](https://img.shields.io/packagist/l/ellipsephp/router-aura.svg?style=plastic)<br>
  * [Ellipse](https://github.com/ellipsephp)/**[FastRoute](https://github.com/ellipsephp/router-fastroute)**
      [![Latest Version on Packagist](https://img.shields.io/packagist/v/ellipsephp/router-fastroute.svg?style=plastic)](https://packagist.org/packages/ellipsephp/router-fastroute)
      ![GitHub last commit](https://img.shields.io/github/last-commit/ellipsephp/router-fastroute.svg?style=plastic)
      ![License](https://img.shields.io/packagist/l/ellipsephp/router-fastroute.svg?style=plastic)<br>

### Security

* [Middlewares](https://github.com/middlewares)/**[Cors](https://github.com/middlewares/cors)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/cors.svg?style=plastic)](https://packagist.org/packages/middlewares/cors)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/cors.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/cors.svg?style=plastic)<br>
    Implements [Cross-Origin Resource Sharing](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing) (CORS) using [neomerx/cors-psr7](https://github.com/neomerx/cors-psr7).
* [Tuupola](https://github.com/tuupola)/**[Cors](https://github.com/tuupola/cors-middleware)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/tuupola/cors-middleware.svg?style=plastic)](https://packagist.org/packages/tuupola/cors-middleware)
    ![GitHub last commit](https://img.shields.io/github/last-commit/tuupola/cors-middleware.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/tuupola/cors-middleware.svg?style=plastic)<br>
    Implements [Cross-Origin Resource Sharing](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing).
* [Middlewares](https://github.com/middlewares)/**[Csp](https://github.com/middlewares/csp)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/csp.svg?style=plastic)](https://packagist.org/packages/middlewares/csp)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/csp.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/csp.svg?style=plastic)<br>
    Adds the [`Content-Security-Policy`](https://content-security-policy.com/) header to the response using [paragonie/csp-builder](https://github.com/paragonie/csp-builder) library. It can also handle the CSP error reports using a [PSR-3 log implementation](https://packagist.org/providers/psr/log-implementation).
* [Grafikart](https://github.com/Grafikart)/**[Csrf](https://github.com/Grafikart/PSR15-CsrfMiddleware)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/grafikart/psr15-csrf-middleware.svg?style=plastic)](https://packagist.org/packages/grafikart/psr15-csrf-middleware)
    ![GitHub last commit](https://img.shields.io/github/last-commit/Grafikart/PSR15-CsrfMiddleware.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/grafikart/psr15-csrf-middleware?style=plastic)<br>
    Checks every `POST`, `PUT` or `DELETE` request for a CSRF token. Tokens are persisted using an `ArrayAccess` compatible session and are generated on demand.
* [Middlewares](https://github.com/middlewares)/**[Firewall](https://github.com/middlewares/firewall)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/firewall.svg?style=plastic)](https://packagist.org/packages/middlewares/firewall)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/firewall.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/firewall.svg?style=plastic)<br>
    Provides IP filtering using [M6Web/Firewall](https://github.com/M6Web/Firewall).
* [Middlewares](https://github.com/middlewares)/**[Honeypot](https://github.com/middlewares/honeypot)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/honeypot.svg?style=plastic)](https://packagist.org/packages/middlewares/honeypot)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/honeypot.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/honeypot.svg?style=plastic)<br>
    Implements honeypot spam prevention. Returns a `403` response if the request is from a bot.
* [Middlewares](https://github.com/middlewares)/**[ReferrerSpam](https://github.com/middlewares/referrer-spam)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/referrer-spam.svg?style=plastic)](https://packagist.org/packages/middlewares/referrer-spam)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/referrer-spam.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/referrer-spam.svg?style=plastic)<br>
    Blocks referrer spammers using [piwik/referrer-spam-blacklist](https://github.com/matomo-org/referrer-spam-blacklist). It returns a 403 response if the URL host in the `Referer` header is in the blacklist.

### Session

* [Middlewares](https://github.com/middlewares)/**[AuraSession](https://github.com/middlewares/aura-session)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/aura-session.svg?style=plastic)](https://packagist.org/packages/middlewares/aura-session)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/aura-session.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/aura-session.svg?style=plastic)<br>
    Manages sessions using [Aura.Session](https://github.com/auraphp/Aura.Session).
* [Middlewares](https://github.com/middlewares)/**[PhpSession](https://github.com/middlewares/php-session)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/php-session.svg?style=plastic)](https://packagist.org/packages/middlewares/php-session)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/php-session.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/php-session.svg?style=plastic)<br>
    Starts a [PHP session](http://php.net/manual/en/book.session.php) using the request data and closes it after returning the response.

### URL

* [Middlewares](https://github.com/middlewares)/**[BasePath](https://github.com/middlewares/base-path)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/base-path.svg?style=plastic)](https://packagist.org/packages/middlewares/base-path)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/base-path.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/base-path.svg?style=plastic)<br>
    Removes the prefix from the URI path of the request. This is useful to combine with routers if the root of the website is in a subdirectory. For example, if the root of the website is `/web/public`, a request with the URI `/web/public/posts/34` will be converted to `/posts/34`.
* [Middlewares](https://github.com/middlewares)/**[Https](https://github.com/middlewares/https)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/https.svg?style=plastic)](https://packagist.org/packages/middlewares/https)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/https.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/https.svg?style=plastic)<br>
    Redirects to `https` if the request is `http` and add the [`Strict-Transport-Security`](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security) header to protect against protocol downgrade attacks and cookie hijacking according to [RFC 6797 HTTP Strict Transport Security (HSTS)](https://tools.ietf.org/html/rfc6797).
* [Middlewares](https://github.com/middlewares)/**[Redirect](https://github.com/middlewares/redirect)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/redirect.svg?style=plastic)](https://packagist.org/packages/middlewares/redirect)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/redirect.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/redirect.svg?style=plastic)<br>
    Redirects old URLs to new URLs in a SEO friendly way.
* [Middlewares](https://github.com/middlewares)/**[TrailingSlash](https://github.com/middlewares/trailing-slash)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/trailing-slash.svg?style=plastic)](https://packagist.org/packages/middlewares/trailing-slash)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/trailing-slash.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/trailing-slash.svg?style=plastic)<br>
    Normalizes the trailing slash of the URI path. By default removes the slash so, for example, `/posts/23/` is converted to `/posts/23`.
* [Middlewares](https://github.com/middlewares)/**[Www](https://github.com/middlewares/www)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/www.svg?style=plastic)](https://packagist.org/packages/middlewares/www)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/www.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/www.svg?style=plastic)<br>
    Adds or removes the `www` subdomain in the host URI and returns a redirect response.

### Miscellaneous

* [Prooph](https://github.com/prooph)/**[HttpMiddleware](https://github.com/prooph/http-middleware)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/prooph/http-middleware.svg?style=plastic)](https://packagist.org/packages/prooph/http-middleware)
    ![GitHub last commit](https://img.shields.io/github/last-commit/prooph/http-middleware.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/prooph/http-middleware.svg?style=plastic)<br>
    Consumes [Prooph](http://getprooph.org/) messages. Contains the following components:
  * [Prooph](https://github.com/prooph)/**[CommandMiddleware](https://github.com/prooph/http-middleware)**<br>
   Dispatches the message data to the command bus system
  * [Prooph](https://github.com/prooph)/**[QueryMiddleware](https://github.com/prooph/http-middleware)**<br>
   Dispatches the message data to the query bus system
  * [Prooph](https://github.com/prooph)/**[EventMiddleware](https://github.com/prooph/http-middleware)**<br>
   Dispatches the message data to the event bus system
  * [Prooph](https://github.com/prooph)/**[MessageMiddleware](https://github.com/prooph/http-middleware)**<br>
   Dispatches the message data to the appropriated bus system depending on message type
* [Middlewares](https://github.com/middlewares)/**[ImageManipulation](https://github.com/middlewares/image-manipulation)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/image-manipulation.svg?style=plastic)](https://packagist.org/packages/middlewares/image-manipulation)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/image-manipulation.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/image-manipulation.svg?style=plastic)<br>
    Transforms images on demand, allowing resize, crop, rotate and transform to other formats. Uses [imagecow](https://github.com/oscarotero/imagecow) library that can detect and use `Gd` and `Imagick`, and also has support for [client hints](https://www.smashingmagazine.com/2016/01/leaner-responsive-images-client-hints/) and different [automatic cropping methods](https://github.com/oscarotero/imagecow#automatic-cropping). The URI is generated encoding the image path and the manipulation options with [lcobucci/jwt](https://github.com/lcobucci/jwt/) to prevent alterations and image-resize attacks.
* [Middlewares](https://github.com/middlewares)/**[MethodOverride](https://github.com/middlewares/method-override)**
    [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/method-override.svg?style=plastic)](https://packagist.org/packages/middlewares/method-override)
    ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/method-override.svg?style=plastic)
    ![License](https://img.shields.io/packagist/l/middlewares/method-override.svg?style=plastic)<br>
    Overrides the request method using the `X-Http-Method-Override` header. This is useful for clients unable to send other methods than `GET` and `POST`.
* [Middlewares](https://github.com/middlewares)/**[Payload](https://github.com/middlewares/payload)**
      [![Latest Version on Packagist](https://img.shields.io/packagist/v/middlewares/payload.svg?style=plastic)](https://packagist.org/packages/middlewares/payload)
      ![GitHub last commit](https://img.shields.io/github/last-commit/middlewares/payload.svg?style=plastic)
      ![License](https://img.shields.io/packagist/l/middlewares/payload.svg?style=plastic)<br>
      Parses the body of the request if it's not already parsed and the method is `POST`, `PUT` or `DELETE`. Contains the following components to support different formats:
  * [Middlewares](https://github.com/middlewares)/**[CsvPayload](https://github.com/middlewares/payload#csvpayload)**
  * [Middlewares](https://github.com/middlewares)/**[JsonPayload](https://github.com/middlewares/payload#jsonpayload)**
  * [Middlewares](https://github.com/middlewares)/**[UrlEncodedPayload](https://github.com/middlewares/payload#urlencodepayload)**



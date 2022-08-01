# composer-smaller-lock

Composer plugin to keep composer.lock small and readable.

[![Latest stable version](https://img.shields.io/packagist/v/kubawerlos/composer-smaller-lock.svg?label=current%20version)](https://packagist.org/packages/kubawerlos/composer-smaller-lock)
[![PHP version](https://img.shields.io/packagist/php-v/kubawerlos/composer-smaller-lock.svg)](https://php.net)
[![CI Status](https://github.com/kubawerlos/composer-smaller-lock/workflows/CI/badge.svg?branch=main&event=push)](https://github.com/kubawerlos/composer-smaller-lock/actions)

Removes unnecessary keys and makes reviewing changes much easier.

[Composer](https://getcomposer.org) writes to the composer.lock a lot of information that it does not need, such as "autoload-dev", "require-dev" and "repositories".
This makes a process of reviewing changes in composer.lock much harder and increases the risk of overlooking important modifications like not wanted (for whatever reason) updates.

## Installation
```bash
composer require --dev kubawerlos/composer-smaller-lock
```

## Usage
None - this is a Composer's plugin, it will subscribe to Composer's events itself.

## Example
<details>
    <summary>Composer's <a href='https://github.com/composer/composer/blob/2.3.10/composer.lock'>composer.lock</a> has 2204 lines, with the plugin the number is reduced to 1118.</summary>

```diff
 {
     "_readme": [
         "This file locks the dependencies of your project to a known state",
         "Read more about it at https://getcomposer.org/doc/01-basic-usage.md#installing-dependencies",
         "This file is @generated automatically"
     ],
     "content-hash": "1f572d2fe0d3c7200c3887bd2fc9e991",
     "packages": [
         {
             "name": "composer/ca-bundle",
             "version": "1.3.2",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/ca-bundle.git",
                 "reference": "fd5dd441932a7e10ca6e5b490e272d34c8430640"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/ca-bundle/zipball/fd5dd441932a7e10ca6e5b490e272d34c8430640",
-                "reference": "fd5dd441932a7e10ca6e5b490e272d34c8430640",
-                "shasum": ""
+                "reference": "fd5dd441932a7e10ca6e5b490e272d34c8430640"
             },
             "require": {
                 "ext-openssl": "*",
                 "ext-pcre": "*",
                 "php": "^5.3.2 || ^7.0 || ^8.0"
             },
-            "require-dev": {
-                "phpstan/phpstan": "^0.12.55",
-                "psr/log": "^1.0",
-                "symfony/phpunit-bridge": "^4.2 || ^5",
-                "symfony/process": "^2.5 || ^3.0 || ^4.0 || ^5.0 || ^6.0"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Composer\\CaBundle\\": "src"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Jordi Boggiano",
-                    "email": "j.boggiano@seld.be",
-                    "homepage": "http://seld.be"
-                }
-            ],
-            "description": "Lets you find a path to the system CA bundle, and includes a fallback to the Mozilla CA bundle.",
-            "keywords": [
-                "cabundle",
-                "cacert",
-                "certificate",
-                "ssl",
-                "tls"
-            ],
-            "support": {
-                "irc": "irc://irc.freenode.org/composer",
-                "issues": "https://github.com/composer/ca-bundle/issues",
-                "source": "https://github.com/composer/ca-bundle/tree/1.3.2"
-            },
-            "funding": [
-                {
-                    "url": "https://packagist.com",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/composer",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/composer/composer",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-24T11:56:16+00:00"
+            "description": "Lets you find a path to the system CA bundle, and includes a fallback to the Mozilla CA bundle."
         },
         {
             "name": "composer/metadata-minifier",
             "version": "1.0.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/metadata-minifier.git",
                 "reference": "c549d23829536f0d0e984aaabbf02af91f443207"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/metadata-minifier/zipball/c549d23829536f0d0e984aaabbf02af91f443207",
-                "reference": "c549d23829536f0d0e984aaabbf02af91f443207",
-                "shasum": ""
+                "reference": "c549d23829536f0d0e984aaabbf02af91f443207"
             },
             "require": {
                 "php": "^5.3.2 || ^7.0 || ^8.0"
             },
-            "require-dev": {
-                "composer/composer": "^2",
-                "phpstan/phpstan": "^0.12.55",
-                "symfony/phpunit-bridge": "^4.2 || ^5"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Composer\\MetadataMinifier\\": "src"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Jordi Boggiano",
-                    "email": "j.boggiano@seld.be",
-                    "homepage": "http://seld.be"
-                }
-            ],
-            "description": "Small utility library that handles metadata minification and expansion.",
-            "keywords": [
-                "composer",
-                "compression"
-            ],
-            "support": {
-                "issues": "https://github.com/composer/metadata-minifier/issues",
-                "source": "https://github.com/composer/metadata-minifier/tree/1.0.0"
-            },
-            "funding": [
-                {
-                    "url": "https://packagist.com",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/composer",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/composer/composer",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2021-04-07T13:37:33+00:00"
+            "description": "Small utility library that handles metadata minification and expansion."
         },
         {
             "name": "composer/pcre",
             "version": "2.0.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/pcre.git",
                 "reference": "c8e9d27cfc5ed22643c19c160455b473ffd8aabe"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/pcre/zipball/c8e9d27cfc5ed22643c19c160455b473ffd8aabe",
-                "reference": "c8e9d27cfc5ed22643c19c160455b473ffd8aabe",
-                "shasum": ""
+                "reference": "c8e9d27cfc5ed22643c19c160455b473ffd8aabe"
             },
             "require": {
                 "php": "^7.2 || ^8.0"
             },
-            "require-dev": {
-                "phpstan/phpstan": "^1.3",
-                "phpstan/phpstan-strict-rules": "^1.1",
-                "symfony/phpunit-bridge": "^5"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "2.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Composer\\Pcre\\": "src"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Jordi Boggiano",
-                    "email": "j.boggiano@seld.be",
-                    "homepage": "http://seld.be"
-                }
-            ],
-            "description": "PCRE wrapping library that offers type-safe preg_* replacements.",
-            "keywords": [
-                "PCRE",
-                "preg",
-                "regex",
-                "regular expression"
-            ],
-            "support": {
-                "issues": "https://github.com/composer/pcre/issues",
-                "source": "https://github.com/composer/pcre/tree/2.0.0"
-            },
-            "funding": [
-                {
-                    "url": "https://packagist.com",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/composer",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/composer/composer",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-02-25T20:05:29+00:00"
+            "description": "PCRE wrapping library that offers type-safe preg_* replacements."
         },
         {
             "name": "composer/semver",
             "version": "3.3.2",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/semver.git",
                 "reference": "3953f23262f2bff1919fc82183ad9acb13ff62c9"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/semver/zipball/3953f23262f2bff1919fc82183ad9acb13ff62c9",
-                "reference": "3953f23262f2bff1919fc82183ad9acb13ff62c9",
-                "shasum": ""
+                "reference": "3953f23262f2bff1919fc82183ad9acb13ff62c9"
             },
             "require": {
                 "php": "^5.3.2 || ^7.0 || ^8.0"
             },
-            "require-dev": {
-                "phpstan/phpstan": "^1.4",
-                "symfony/phpunit-bridge": "^4.2 || ^5"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "3.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Composer\\Semver\\": "src"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nils Adermann",
-                    "email": "naderman@naderman.de",
-                    "homepage": "http://www.naderman.de"
-                },
-                {
-                    "name": "Jordi Boggiano",
-                    "email": "j.boggiano@seld.be",
-                    "homepage": "http://seld.be"
-                },
-                {
-                    "name": "Rob Bast",
-                    "email": "rob.bast@gmail.com",
-                    "homepage": "http://robbast.nl"
-                }
-            ],
-            "description": "Semver library that offers utilities, version constraint parsing and validation.",
-            "keywords": [
-                "semantic",
-                "semver",
-                "validation",
-                "versioning"
-            ],
-            "support": {
-                "irc": "irc://irc.freenode.org/composer",
-                "issues": "https://github.com/composer/semver/issues",
-                "source": "https://github.com/composer/semver/tree/3.3.2"
-            },
-            "funding": [
-                {
-                    "url": "https://packagist.com",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/composer",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/composer/composer",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-04-01T19:23:25+00:00"
+            "description": "Semver library that offers utilities, version constraint parsing and validation."
         },
         {
             "name": "composer/spdx-licenses",
             "version": "1.5.7",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/spdx-licenses.git",
                 "reference": "c848241796da2abf65837d51dce1fae55a960149"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/spdx-licenses/zipball/c848241796da2abf65837d51dce1fae55a960149",
-                "reference": "c848241796da2abf65837d51dce1fae55a960149",
-                "shasum": ""
+                "reference": "c848241796da2abf65837d51dce1fae55a960149"
             },
             "require": {
                 "php": "^5.3.2 || ^7.0 || ^8.0"
             },
-            "require-dev": {
-                "phpstan/phpstan": "^0.12.55",
-                "symfony/phpunit-bridge": "^4.2 || ^5"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Composer\\Spdx\\": "src"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nils Adermann",
-                    "email": "naderman@naderman.de",
-                    "homepage": "http://www.naderman.de"
-                },
-                {
-                    "name": "Jordi Boggiano",
-                    "email": "j.boggiano@seld.be",
-                    "homepage": "http://seld.be"
-                },
-                {
-                    "name": "Rob Bast",
-                    "email": "rob.bast@gmail.com",
-                    "homepage": "http://robbast.nl"
-                }
-            ],
-            "description": "SPDX licenses list and validation library.",
-            "keywords": [
-                "license",
-                "spdx",
-                "validator"
-            ],
-            "support": {
-                "irc": "irc://irc.freenode.org/composer",
-                "issues": "https://github.com/composer/spdx-licenses/issues",
-                "source": "https://github.com/composer/spdx-licenses/tree/1.5.7"
-            },
-            "funding": [
-                {
-                    "url": "https://packagist.com",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/composer",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/composer/composer",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-23T07:37:50+00:00"
+            "description": "SPDX licenses list and validation library."
         },
         {
             "name": "composer/xdebug-handler",
             "version": "3.0.3",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/xdebug-handler.git",
                 "reference": "ced299686f41dce890debac69273b47ffe98a40c"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/xdebug-handler/zipball/ced299686f41dce890debac69273b47ffe98a40c",
-                "reference": "ced299686f41dce890debac69273b47ffe98a40c",
-                "shasum": ""
+                "reference": "ced299686f41dce890debac69273b47ffe98a40c"
             },
             "require": {
                 "composer/pcre": "^1 || ^2 || ^3",
                 "php": "^7.2.5 || ^8.0",
                 "psr/log": "^1 || ^2 || ^3"
             },
-            "require-dev": {
-                "phpstan/phpstan": "^1.0",
-                "phpstan/phpstan-strict-rules": "^1.1",
-                "symfony/phpunit-bridge": "^6.0"
-            },
             "type": "library",
             "autoload": {
                 "psr-4": {
                     "Composer\\XdebugHandler\\": "src"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "John Stevenson",
-                    "email": "john-stevenson@blueyonder.co.uk"
-                }
-            ],
-            "description": "Restarts a process without Xdebug.",
-            "keywords": [
-                "Xdebug",
-                "performance"
-            ],
-            "support": {
-                "irc": "irc://irc.freenode.org/composer",
-                "issues": "https://github.com/composer/xdebug-handler/issues",
-                "source": "https://github.com/composer/xdebug-handler/tree/3.0.3"
-            },
-            "funding": [
-                {
-                    "url": "https://packagist.com",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/composer",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/composer/composer",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-02-25T21:32:43+00:00"
+            "description": "Restarts a process without Xdebug."
         },
         {
             "name": "justinrainbow/json-schema",
             "version": "5.2.12",
             "source": {
                 "type": "git",
                 "url": "https://github.com/justinrainbow/json-schema.git",
                 "reference": "ad87d5a5ca981228e0e205c2bc7dfb8e24559b60"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/justinrainbow/json-schema/zipball/ad87d5a5ca981228e0e205c2bc7dfb8e24559b60",
-                "reference": "ad87d5a5ca981228e0e205c2bc7dfb8e24559b60",
-                "shasum": ""
+                "reference": "ad87d5a5ca981228e0e205c2bc7dfb8e24559b60"
             },
             "require": {
                 "php": ">=5.3.3"
             },
-            "require-dev": {
-                "friendsofphp/php-cs-fixer": "~2.2.20||~2.15.1",
-                "json-schema/json-schema-test-suite": "1.2.0",
-                "phpunit/phpunit": "^4.8.35"
-            },
             "bin": [
                 "bin/validate-json"
             ],
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "5.0.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "JsonSchema\\": "src/JsonSchema/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Bruno Prieto Reis",
-                    "email": "bruno.p.reis@gmail.com"
-                },
-                {
-                    "name": "Justin Rainbow",
-                    "email": "justin.rainbow@gmail.com"
-                },
-                {
-                    "name": "Igor Wiedler",
-                    "email": "igor@wiedler.ch"
-                },
-                {
-                    "name": "Robert Schönthal",
-                    "email": "seroscho@googlemail.com"
-                }
-            ],
-            "description": "A library to validate a json schema.",
-            "homepage": "https://github.com/justinrainbow/json-schema",
-            "keywords": [
-                "json",
-                "schema"
-            ],
-            "support": {
-                "issues": "https://github.com/justinrainbow/json-schema/issues",
-                "source": "https://github.com/justinrainbow/json-schema/tree/5.2.12"
-            },
-            "time": "2022-04-13T08:02:27+00:00"
+            "description": "A library to validate a json schema."
         },
         {
             "name": "psr/container",
             "version": "1.1.1",
             "source": {
                 "type": "git",
                 "url": "https://github.com/php-fig/container.git",
                 "reference": "8622567409010282b7aeebe4bb841fe98b58dcaf"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/php-fig/container/zipball/8622567409010282b7aeebe4bb841fe98b58dcaf",
-                "reference": "8622567409010282b7aeebe4bb841fe98b58dcaf",
-                "shasum": ""
+                "reference": "8622567409010282b7aeebe4bb841fe98b58dcaf"
             },
             "require": {
                 "php": ">=7.2.0"
             },
             "type": "library",
             "autoload": {
                 "psr-4": {
                     "Psr\\Container\\": "src/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "PHP-FIG",
-                    "homepage": "https://www.php-fig.org/"
-                }
-            ],
-            "description": "Common Container Interface (PHP FIG PSR-11)",
-            "homepage": "https://github.com/php-fig/container",
-            "keywords": [
-                "PSR-11",
-                "container",
-                "container-interface",
-                "container-interop",
-                "psr"
-            ],
-            "support": {
-                "issues": "https://github.com/php-fig/container/issues",
-                "source": "https://github.com/php-fig/container/tree/1.1.1"
-            },
-            "time": "2021-03-05T17:36:06+00:00"
+            "description": "Common Container Interface (PHP FIG PSR-11)"
         },
         {
             "name": "psr/log",
             "version": "1.1.4",
             "source": {
                 "type": "git",
                 "url": "https://github.com/php-fig/log.git",
                 "reference": "d49695b909c3b7628b6289db5479a1c204601f11"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/php-fig/log/zipball/d49695b909c3b7628b6289db5479a1c204601f11",
-                "reference": "d49695b909c3b7628b6289db5479a1c204601f11",
-                "shasum": ""
+                "reference": "d49695b909c3b7628b6289db5479a1c204601f11"
             },
             "require": {
                 "php": ">=5.3.0"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "1.1.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Psr\\Log\\": "Psr/Log/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "PHP-FIG",
-                    "homepage": "https://www.php-fig.org/"
-                }
-            ],
-            "description": "Common interface for logging libraries",
-            "homepage": "https://github.com/php-fig/log",
-            "keywords": [
-                "log",
-                "psr",
-                "psr-3"
-            ],
-            "support": {
-                "source": "https://github.com/php-fig/log/tree/1.1.4"
-            },
-            "time": "2021-05-03T11:20:27+00:00"
+            "description": "Common interface for logging libraries"
         },
         {
             "name": "react/promise",
             "version": "v2.9.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/reactphp/promise.git",
                 "reference": "234f8fd1023c9158e2314fa9d7d0e6a83db42910"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/reactphp/promise/zipball/234f8fd1023c9158e2314fa9d7d0e6a83db42910",
-                "reference": "234f8fd1023c9158e2314fa9d7d0e6a83db42910",
-                "shasum": ""
+                "reference": "234f8fd1023c9158e2314fa9d7d0e6a83db42910"
             },
             "require": {
                 "php": ">=5.4.0"
             },
-            "require-dev": {
-                "phpunit/phpunit": "^9.3 || ^5.7 || ^4.8.36"
-            },
             "type": "library",
             "autoload": {
                 "files": [
                     "src/functions_include.php"
                 ],
                 "psr-4": {
                     "React\\Promise\\": "src/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Jan Sorgalla",
-                    "email": "jsorgalla@gmail.com",
-                    "homepage": "https://sorgalla.com/"
-                },
-                {
-                    "name": "Christian Lück",
-                    "email": "christian@clue.engineering",
-                    "homepage": "https://clue.engineering/"
-                },
-                {
-                    "name": "Cees-Jan Kiewiet",
-                    "email": "reactphp@ceesjankiewiet.nl",
-                    "homepage": "https://wyrihaximus.net/"
-                },
-                {
-                    "name": "Chris Boden",
-                    "email": "cboden@gmail.com",
-                    "homepage": "https://cboden.dev/"
-                }
-            ],
-            "description": "A lightweight implementation of CommonJS Promises/A for PHP",
-            "keywords": [
-                "promise",
-                "promises"
-            ],
-            "support": {
-                "issues": "https://github.com/reactphp/promise/issues",
-                "source": "https://github.com/reactphp/promise/tree/v2.9.0"
-            },
-            "funding": [
-                {
-                    "url": "https://github.com/WyriHaximus",
-                    "type": "github"
-                },
-                {
-                    "url": "https://github.com/clue",
-                    "type": "github"
-                }
-            ],
-            "time": "2022-02-11T10:27:51+00:00"
+            "description": "A lightweight implementation of CommonJS Promises/A for PHP"
         },
         {
             "name": "seld/jsonlint",
             "version": "1.9.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/Seldaek/jsonlint.git",
                 "reference": "4211420d25eba80712bff236a98960ef68b866b7"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/Seldaek/jsonlint/zipball/4211420d25eba80712bff236a98960ef68b866b7",
-                "reference": "4211420d25eba80712bff236a98960ef68b866b7",
-                "shasum": ""
+                "reference": "4211420d25eba80712bff236a98960ef68b866b7"
             },
             "require": {
                 "php": "^5.3 || ^7.0 || ^8.0"
             },
-            "require-dev": {
-                "phpstan/phpstan": "^1.5",
-                "phpunit/phpunit": "^4.8.35 || ^5.7 || ^6.0 || ^8.5.13"
-            },
             "bin": [
                 "bin/jsonlint"
             ],
             "type": "library",
             "autoload": {
                 "psr-4": {
                     "Seld\\JsonLint\\": "src/Seld/JsonLint/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Jordi Boggiano",
-                    "email": "j.boggiano@seld.be",
-                    "homepage": "http://seld.be"
-                }
-            ],
-            "description": "JSON Linter",
-            "keywords": [
-                "json",
-                "linter",
-                "parser",
-                "validator"
-            ],
-            "support": {
-                "issues": "https://github.com/Seldaek/jsonlint/issues",
-                "source": "https://github.com/Seldaek/jsonlint/tree/1.9.0"
-            },
-            "funding": [
-                {
-                    "url": "https://github.com/Seldaek",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/seld/jsonlint",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-04-01T13:37:23+00:00"
+            "description": "JSON Linter"
         },
         {
             "name": "seld/phar-utils",
             "version": "1.2.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/Seldaek/phar-utils.git",
                 "reference": "9f3452c93ff423469c0d56450431562ca423dcee"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/Seldaek/phar-utils/zipball/9f3452c93ff423469c0d56450431562ca423dcee",
-                "reference": "9f3452c93ff423469c0d56450431562ca423dcee",
-                "shasum": ""
+                "reference": "9f3452c93ff423469c0d56450431562ca423dcee"
             },
             "require": {
                 "php": ">=5.3"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "1.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Seld\\PharUtils\\": "src/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Jordi Boggiano",
-                    "email": "j.boggiano@seld.be"
-                }
-            ],
-            "description": "PHAR file format utilities, for when PHP phars you up",
-            "keywords": [
-                "phar"
-            ],
-            "support": {
-                "issues": "https://github.com/Seldaek/phar-utils/issues",
-                "source": "https://github.com/Seldaek/phar-utils/tree/1.2.0"
-            },
-            "time": "2021-12-10T11:20:11+00:00"
+            "description": "PHAR file format utilities, for when PHP phars you up"
         },
         {
             "name": "symfony/console",
             "version": "v5.4.9",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/console.git",
                 "reference": "829d5d1bf60b2efeb0887b7436873becc71a45eb"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/console/zipball/829d5d1bf60b2efeb0887b7436873becc71a45eb",
-                "reference": "829d5d1bf60b2efeb0887b7436873becc71a45eb",
-                "shasum": ""
+                "reference": "829d5d1bf60b2efeb0887b7436873becc71a45eb"
             },
             "require": {
                 "php": ">=7.2.5",
                 "symfony/deprecation-contracts": "^2.1|^3",
                 "symfony/polyfill-mbstring": "~1.0",
                 "symfony/polyfill-php73": "^1.9",
                 "symfony/polyfill-php80": "^1.16",
                 "symfony/service-contracts": "^1.1|^2|^3",
                 "symfony/string": "^5.1|^6.0"
             },
-            "conflict": {
-                "psr/log": ">=3",
-                "symfony/dependency-injection": "<4.4",
-                "symfony/dotenv": "<5.1",
-                "symfony/event-dispatcher": "<4.4",
-                "symfony/lock": "<4.4",
-                "symfony/process": "<4.4"
-            },
             "provide": {
                 "psr/log-implementation": "1.0|2.0"
             },
-            "require-dev": {
-                "psr/log": "^1|^2",
-                "symfony/config": "^4.4|^5.0|^6.0",
-                "symfony/dependency-injection": "^4.4|^5.0|^6.0",
-                "symfony/event-dispatcher": "^4.4|^5.0|^6.0",
-                "symfony/lock": "^4.4|^5.0|^6.0",
-                "symfony/process": "^4.4|^5.0|^6.0",
-                "symfony/var-dumper": "^4.4|^5.0|^6.0"
-            },
-            "suggest": {
-                "psr/log": "For using the console logger",
-                "symfony/event-dispatcher": "",
-                "symfony/lock": "",
-                "symfony/process": ""
-            },
             "type": "library",
             "autoload": {
                 "psr-4": {
                     "Symfony\\Component\\Console\\": ""
                 },
                 "exclude-from-classmap": [
                     "/Tests/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Fabien Potencier",
-                    "email": "fabien@symfony.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Eases the creation of beautiful and testable command line interfaces",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "cli",
-                "command line",
-                "console",
-                "terminal"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/console/tree/v5.4.9"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-18T06:17:34+00:00"
+            "description": "Eases the creation of beautiful and testable command line interfaces"
         },
         {
             "name": "symfony/deprecation-contracts",
             "version": "v2.5.1",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/deprecation-contracts.git",
                 "reference": "e8b495ea28c1d97b5e0c121748d6f9b53d075c66"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/deprecation-contracts/zipball/e8b495ea28c1d97b5e0c121748d6f9b53d075c66",
-                "reference": "e8b495ea28c1d97b5e0c121748d6f9b53d075c66",
-                "shasum": ""
+                "reference": "e8b495ea28c1d97b5e0c121748d6f9b53d075c66"
             },
             "require": {
                 "php": ">=7.1"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "2.5-dev"
                 },
                 "thanks": {
                     "name": "symfony/contracts",
                     "url": "https://github.com/symfony/contracts"
                 }
             },
             "autoload": {
                 "files": [
                     "function.php"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "A generic function and convention to trigger deprecation notices",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/deprecation-contracts/tree/v2.5.1"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-01-02T09:53:40+00:00"
+            "description": "A generic function and convention to trigger deprecation notices"
         },
         {
             "name": "symfony/filesystem",
             "version": "v5.4.9",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/filesystem.git",
                 "reference": "36a017fa4cce1eff1b8e8129ff53513abcef05ba"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/filesystem/zipball/36a017fa4cce1eff1b8e8129ff53513abcef05ba",
-                "reference": "36a017fa4cce1eff1b8e8129ff53513abcef05ba",
-                "shasum": ""
+                "reference": "36a017fa4cce1eff1b8e8129ff53513abcef05ba"
             },
             "require": {
                 "php": ">=7.2.5",
                 "symfony/polyfill-ctype": "~1.8",
                 "symfony/polyfill-mbstring": "~1.8",
                 "symfony/polyfill-php80": "^1.16"
             },
             "type": "library",
             "autoload": {
                 "psr-4": {
                     "Symfony\\Component\\Filesystem\\": ""
                 },
                 "exclude-from-classmap": [
                     "/Tests/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Fabien Potencier",
-                    "email": "fabien@symfony.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Provides basic utilities for the filesystem",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/filesystem/tree/v5.4.9"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-20T13:55:35+00:00"
+            "description": "Provides basic utilities for the filesystem"
         },
         {
             "name": "symfony/finder",
             "version": "v5.4.8",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/finder.git",
                 "reference": "9b630f3427f3ebe7cd346c277a1408b00249dad9"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/finder/zipball/9b630f3427f3ebe7cd346c277a1408b00249dad9",
-                "reference": "9b630f3427f3ebe7cd346c277a1408b00249dad9",
-                "shasum": ""
+                "reference": "9b630f3427f3ebe7cd346c277a1408b00249dad9"
             },
             "require": {
                 "php": ">=7.2.5",
                 "symfony/deprecation-contracts": "^2.1|^3",
                 "symfony/polyfill-php80": "^1.16"
             },
             "type": "library",
             "autoload": {
                 "psr-4": {
                     "Symfony\\Component\\Finder\\": ""
                 },
                 "exclude-from-classmap": [
                     "/Tests/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Fabien Potencier",
-                    "email": "fabien@symfony.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Finds files and directories via an intuitive fluent interface",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/finder/tree/v5.4.8"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-04-15T08:07:45+00:00"
+            "description": "Finds files and directories via an intuitive fluent interface"
         },
         {
             "name": "symfony/polyfill-ctype",
             "version": "v1.26.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/polyfill-ctype.git",
                 "reference": "6fd1b9a79f6e3cf65f9e679b23af304cd9e010d4"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/polyfill-ctype/zipball/6fd1b9a79f6e3cf65f9e679b23af304cd9e010d4",
-                "reference": "6fd1b9a79f6e3cf65f9e679b23af304cd9e010d4",
-                "shasum": ""
+                "reference": "6fd1b9a79f6e3cf65f9e679b23af304cd9e010d4"
             },
             "require": {
                 "php": ">=7.1"
             },
             "provide": {
                 "ext-ctype": "*"
             },
-            "suggest": {
-                "ext-ctype": "For best performance"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.26-dev"
                 },
                 "thanks": {
                     "name": "symfony/polyfill",
                     "url": "https://github.com/symfony/polyfill"
                 }
             },
             "autoload": {
                 "files": [
                     "bootstrap.php"
                 ],
                 "psr-4": {
                     "Symfony\\Polyfill\\Ctype\\": ""
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Gert de Pagter",
-                    "email": "BackEndTea@gmail.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Symfony polyfill for ctype functions",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "compatibility",
-                "ctype",
-                "polyfill",
-                "portable"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/polyfill-ctype/tree/v1.26.0"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-24T11:49:31+00:00"
+            "description": "Symfony polyfill for ctype functions"
         },
         {
             "name": "symfony/polyfill-intl-grapheme",
             "version": "v1.26.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/polyfill-intl-grapheme.git",
                 "reference": "433d05519ce6990bf3530fba6957499d327395c2"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/polyfill-intl-grapheme/zipball/433d05519ce6990bf3530fba6957499d327395c2",
-                "reference": "433d05519ce6990bf3530fba6957499d327395c2",
-                "shasum": ""
+                "reference": "433d05519ce6990bf3530fba6957499d327395c2"
             },
             "require": {
                 "php": ">=7.1"
             },
-            "suggest": {
-                "ext-intl": "For best performance"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.26-dev"
                 },
                 "thanks": {
                     "name": "symfony/polyfill",
                     "url": "https://github.com/symfony/polyfill"
                 }
             },
             "autoload": {
                 "files": [
                     "bootstrap.php"
                 ],
                 "psr-4": {
                     "Symfony\\Polyfill\\Intl\\Grapheme\\": ""
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Symfony polyfill for intl's grapheme_* functions",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "compatibility",
-                "grapheme",
-                "intl",
-                "polyfill",
-                "portable",
-                "shim"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/polyfill-intl-grapheme/tree/v1.26.0"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-24T11:49:31+00:00"
+            "description": "Symfony polyfill for intl's grapheme_* functions"
         },
         {
             "name": "symfony/polyfill-intl-normalizer",
             "version": "v1.26.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/polyfill-intl-normalizer.git",
                 "reference": "219aa369ceff116e673852dce47c3a41794c14bd"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/polyfill-intl-normalizer/zipball/219aa369ceff116e673852dce47c3a41794c14bd",
-                "reference": "219aa369ceff116e673852dce47c3a41794c14bd",
-                "shasum": ""
+                "reference": "219aa369ceff116e673852dce47c3a41794c14bd"
             },
             "require": {
                 "php": ">=7.1"
             },
-            "suggest": {
-                "ext-intl": "For best performance"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.26-dev"
                 },
                 "thanks": {
                     "name": "symfony/polyfill",
                     "url": "https://github.com/symfony/polyfill"
                 }
             },
             "autoload": {
                 "files": [
                     "bootstrap.php"
                 ],
                 "psr-4": {
                     "Symfony\\Polyfill\\Intl\\Normalizer\\": ""
                 },
                 "classmap": [
                     "Resources/stubs"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Symfony polyfill for intl's Normalizer class and related functions",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "compatibility",
-                "intl",
-                "normalizer",
-                "polyfill",
-                "portable",
-                "shim"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/polyfill-intl-normalizer/tree/v1.26.0"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-24T11:49:31+00:00"
+            "description": "Symfony polyfill for intl's Normalizer class and related functions"
         },
         {
             "name": "symfony/polyfill-mbstring",
             "version": "v1.26.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/polyfill-mbstring.git",
                 "reference": "9344f9cb97f3b19424af1a21a3b0e75b0a7d8d7e"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/polyfill-mbstring/zipball/9344f9cb97f3b19424af1a21a3b0e75b0a7d8d7e",
-                "reference": "9344f9cb97f3b19424af1a21a3b0e75b0a7d8d7e",
-                "shasum": ""
+                "reference": "9344f9cb97f3b19424af1a21a3b0e75b0a7d8d7e"
             },
             "require": {
                 "php": ">=7.1"
             },
             "provide": {
                 "ext-mbstring": "*"
             },
-            "suggest": {
-                "ext-mbstring": "For best performance"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.26-dev"
                 },
                 "thanks": {
                     "name": "symfony/polyfill",
                     "url": "https://github.com/symfony/polyfill"
                 }
             },
             "autoload": {
                 "files": [
                     "bootstrap.php"
                 ],
                 "psr-4": {
                     "Symfony\\Polyfill\\Mbstring\\": ""
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Symfony polyfill for the Mbstring extension",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "compatibility",
-                "mbstring",
-                "polyfill",
-                "portable",
-                "shim"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/polyfill-mbstring/tree/v1.26.0"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-24T11:49:31+00:00"
+            "description": "Symfony polyfill for the Mbstring extension"
         },
         {
             "name": "symfony/polyfill-php73",
             "version": "v1.26.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/polyfill-php73.git",
                 "reference": "e440d35fa0286f77fb45b79a03fedbeda9307e85"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/polyfill-php73/zipball/e440d35fa0286f77fb45b79a03fedbeda9307e85",
-                "reference": "e440d35fa0286f77fb45b79a03fedbeda9307e85",
-                "shasum": ""
+                "reference": "e440d35fa0286f77fb45b79a03fedbeda9307e85"
             },
             "require": {
                 "php": ">=7.1"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.26-dev"
                 },
                 "thanks": {
                     "name": "symfony/polyfill",
                     "url": "https://github.com/symfony/polyfill"
                 }
             },
             "autoload": {
                 "files": [
                     "bootstrap.php"
                 ],
                 "psr-4": {
                     "Symfony\\Polyfill\\Php73\\": ""
                 },
                 "classmap": [
                     "Resources/stubs"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Symfony polyfill backporting some PHP 7.3+ features to lower PHP versions",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "compatibility",
-                "polyfill",
-                "portable",
-                "shim"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/polyfill-php73/tree/v1.26.0"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-24T11:49:31+00:00"
+            "description": "Symfony polyfill backporting some PHP 7.3+ features to lower PHP versions"
         },
         {
             "name": "symfony/polyfill-php80",
             "version": "v1.26.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/polyfill-php80.git",
                 "reference": "cfa0ae98841b9e461207c13ab093d76b0fa7bace"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/polyfill-php80/zipball/cfa0ae98841b9e461207c13ab093d76b0fa7bace",
-                "reference": "cfa0ae98841b9e461207c13ab093d76b0fa7bace",
-                "shasum": ""
+                "reference": "cfa0ae98841b9e461207c13ab093d76b0fa7bace"
             },
             "require": {
                 "php": ">=7.1"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.26-dev"
                 },
                 "thanks": {
                     "name": "symfony/polyfill",
                     "url": "https://github.com/symfony/polyfill"
                 }
             },
             "autoload": {
                 "files": [
                     "bootstrap.php"
                 ],
                 "psr-4": {
                     "Symfony\\Polyfill\\Php80\\": ""
                 },
                 "classmap": [
                     "Resources/stubs"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Ion Bazan",
-                    "email": "ion.bazan@gmail.com"
-                },
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Symfony polyfill backporting some PHP 8.0+ features to lower PHP versions",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "compatibility",
-                "polyfill",
-                "portable",
-                "shim"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/polyfill-php80/tree/v1.26.0"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-05-10T07:21:04+00:00"
+            "description": "Symfony polyfill backporting some PHP 8.0+ features to lower PHP versions"
         },
         {
             "name": "symfony/process",
             "version": "v5.4.8",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/process.git",
                 "reference": "597f3fff8e3e91836bb0bd38f5718b56ddbde2f3"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/process/zipball/597f3fff8e3e91836bb0bd38f5718b56ddbde2f3",
-                "reference": "597f3fff8e3e91836bb0bd38f5718b56ddbde2f3",
-                "shasum": ""
+                "reference": "597f3fff8e3e91836bb0bd38f5718b56ddbde2f3"
             },
             "require": {
                 "php": ">=7.2.5",
                 "symfony/polyfill-php80": "^1.16"
             },
             "type": "library",
             "autoload": {
                 "psr-4": {
                     "Symfony\\Component\\Process\\": ""
                 },
                 "exclude-from-classmap": [
                     "/Tests/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Fabien Potencier",
-                    "email": "fabien@symfony.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Executes commands in sub-processes",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/process/tree/v5.4.8"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-04-08T05:07:18+00:00"
+            "description": "Executes commands in sub-processes"
         },
         {
             "name": "symfony/service-contracts",
             "version": "v2.5.1",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/service-contracts.git",
                 "reference": "24d9dc654b83e91aa59f9d167b131bc3b5bea24c"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/service-contracts/zipball/24d9dc654b83e91aa59f9d167b131bc3b5bea24c",
-                "reference": "24d9dc654b83e91aa59f9d167b131bc3b5bea24c",
-                "shasum": ""
+                "reference": "24d9dc654b83e91aa59f9d167b131bc3b5bea24c"
             },
             "require": {
                 "php": ">=7.2.5",
                 "psr/container": "^1.1",
                 "symfony/deprecation-contracts": "^2.1|^3"
             },
-            "conflict": {
-                "ext-psr": "<1.1|>=2"
-            },
-            "suggest": {
-                "symfony/service-implementation": ""
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "2.5-dev"
                 },
                 "thanks": {
                     "name": "symfony/contracts",
                     "url": "https://github.com/symfony/contracts"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Symfony\\Contracts\\Service\\": ""
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Generic abstractions related to writing services",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "abstractions",
-                "contracts",
-                "decoupling",
-                "interfaces",
-                "interoperability",
-                "standards"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/service-contracts/tree/v2.5.1"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-03-13T20:07:29+00:00"
+            "description": "Generic abstractions related to writing services"
         },
         {
             "name": "symfony/string",
             "version": "v5.4.9",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/string.git",
                 "reference": "985e6a9703ef5ce32ba617c9c7d97873bb7b2a99"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/string/zipball/985e6a9703ef5ce32ba617c9c7d97873bb7b2a99",
-                "reference": "985e6a9703ef5ce32ba617c9c7d97873bb7b2a99",
-                "shasum": ""
+                "reference": "985e6a9703ef5ce32ba617c9c7d97873bb7b2a99"
             },
             "require": {
                 "php": ">=7.2.5",
                 "symfony/polyfill-ctype": "~1.8",
                 "symfony/polyfill-intl-grapheme": "~1.0",
                 "symfony/polyfill-intl-normalizer": "~1.0",
                 "symfony/polyfill-mbstring": "~1.0",
                 "symfony/polyfill-php80": "~1.15"
             },
-            "conflict": {
-                "symfony/translation-contracts": ">=3.0"
-            },
-            "require-dev": {
-                "symfony/error-handler": "^4.4|^5.0|^6.0",
-                "symfony/http-client": "^4.4|^5.0|^6.0",
-                "symfony/translation-contracts": "^1.1|^2",
-                "symfony/var-exporter": "^4.4|^5.0|^6.0"
-            },
             "type": "library",
             "autoload": {
                 "files": [
                     "Resources/functions.php"
                 ],
                 "psr-4": {
                     "Symfony\\Component\\String\\": ""
                 },
                 "exclude-from-classmap": [
                     "/Tests/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Provides an object-oriented API to strings and deals with bytes, UTF-8 code points and grapheme clusters in a unified way",
-            "homepage": "https://symfony.com",
-            "keywords": [
-                "grapheme",
-                "i18n",
-                "string",
-                "unicode",
-                "utf-8",
-                "utf8"
-            ],
-            "support": {
-                "source": "https://github.com/symfony/string/tree/v5.4.9"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-04-19T10:40:37+00:00"
+            "description": "Provides an object-oriented API to strings and deals with bytes, UTF-8 code points and grapheme clusters in a unified way"
         }
     ],
     "packages-dev": [
         {
             "name": "phpstan/phpstan",
             "version": "1.7.15",
             "source": {
                 "type": "git",
                 "url": "https://github.com/phpstan/phpstan.git",
                 "reference": "cd0202ea1b1fc6d1bbe156c6e2e18a03e0ff160a"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/phpstan/phpstan/zipball/cd0202ea1b1fc6d1bbe156c6e2e18a03e0ff160a",
-                "reference": "cd0202ea1b1fc6d1bbe156c6e2e18a03e0ff160a",
-                "shasum": ""
+                "reference": "cd0202ea1b1fc6d1bbe156c6e2e18a03e0ff160a"
             },
             "require": {
                 "php": "^7.2|^8.0"
             },
-            "conflict": {
-                "phpstan/phpstan-shim": "*"
-            },
             "bin": [
                 "phpstan",
                 "phpstan.phar"
             ],
             "type": "library",
             "autoload": {
                 "files": [
                     "bootstrap.php"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "description": "PHPStan - PHP Static Analysis Tool",
-            "support": {
-                "issues": "https://github.com/phpstan/phpstan/issues",
-                "source": "https://github.com/phpstan/phpstan/tree/1.7.15"
-            },
-            "funding": [
-                {
-                    "url": "https://github.com/ondrejmirtes",
-                    "type": "github"
-                },
-                {
-                    "url": "https://github.com/phpstan",
-                    "type": "github"
-                },
-                {
-                    "url": "https://www.patreon.com/phpstan",
-                    "type": "patreon"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/phpstan/phpstan",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-06-20T08:29:01+00:00"
+            "description": "PHPStan - PHP Static Analysis Tool"
         },
         {
             "name": "phpstan/phpstan-deprecation-rules",
             "version": "1.0.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/phpstan/phpstan-deprecation-rules.git",
                 "reference": "e5ccafb0dd8d835dd65d8d7a1a0d2b1b75414682"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/phpstan/phpstan-deprecation-rules/zipball/e5ccafb0dd8d835dd65d8d7a1a0d2b1b75414682",
-                "reference": "e5ccafb0dd8d835dd65d8d7a1a0d2b1b75414682",
-                "shasum": ""
+                "reference": "e5ccafb0dd8d835dd65d8d7a1a0d2b1b75414682"
             },
             "require": {
                 "php": "^7.1 || ^8.0",
                 "phpstan/phpstan": "^1.0"
             },
-            "require-dev": {
-                "php-parallel-lint/php-parallel-lint": "^1.2",
-                "phpstan/phpstan-phpunit": "^1.0",
-                "phpunit/phpunit": "^9.5"
-            },
             "type": "phpstan-extension",
             "extra": {
                 "branch-alias": {
                     "dev-master": "1.0-dev"
                 },
                 "phpstan": {
                     "includes": [
                         "rules.neon"
                     ]
                 }
             },
             "autoload": {
                 "psr-4": {
                     "PHPStan\\": "src/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "description": "PHPStan rules for detecting usage of deprecated classes, methods, properties, constants and traits.",
-            "support": {
-                "issues": "https://github.com/phpstan/phpstan-deprecation-rules/issues",
-                "source": "https://github.com/phpstan/phpstan-deprecation-rules/tree/1.0.0"
-            },
-            "time": "2021-09-23T11:02:21+00:00"
+            "description": "PHPStan rules for detecting usage of deprecated classes, methods, properties, constants and traits."
         },
         {
             "name": "phpstan/phpstan-phpunit",
             "version": "1.1.1",
             "source": {
                 "type": "git",
                 "url": "https://github.com/phpstan/phpstan-phpunit.git",
                 "reference": "4a3c437c09075736285d1cabb5c75bf27ed0bc84"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/phpstan/phpstan-phpunit/zipball/4a3c437c09075736285d1cabb5c75bf27ed0bc84",
-                "reference": "4a3c437c09075736285d1cabb5c75bf27ed0bc84",
-                "shasum": ""
+                "reference": "4a3c437c09075736285d1cabb5c75bf27ed0bc84"
             },
             "require": {
                 "php": "^7.2 || ^8.0",
                 "phpstan/phpstan": "^1.5.0"
             },
-            "conflict": {
-                "phpunit/phpunit": "<7.0"
-            },
-            "require-dev": {
-                "nikic/php-parser": "^4.13.0",
-                "php-parallel-lint/php-parallel-lint": "^1.2",
-                "phpstan/phpstan-strict-rules": "^1.0",
-                "phpunit/phpunit": "^9.5"
-            },
             "type": "phpstan-extension",
             "extra": {
                 "phpstan": {
                     "includes": [
                         "extension.neon",
                         "rules.neon"
                     ]
                 }
             },
             "autoload": {
                 "psr-4": {
                     "PHPStan\\": "src/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "description": "PHPUnit extensions and rules for PHPStan",
-            "support": {
-                "issues": "https://github.com/phpstan/phpstan-phpunit/issues",
-                "source": "https://github.com/phpstan/phpstan-phpunit/tree/1.1.1"
-            },
-            "time": "2022-04-20T15:24:25+00:00"
+            "description": "PHPUnit extensions and rules for PHPStan"
         },
         {
             "name": "phpstan/phpstan-strict-rules",
             "version": "1.2.3",
             "source": {
                 "type": "git",
                 "url": "https://github.com/phpstan/phpstan-strict-rules.git",
                 "reference": "0c82c96f2a55d8b91bbc7ee6512c94f68a206b43"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/phpstan/phpstan-strict-rules/zipball/0c82c96f2a55d8b91bbc7ee6512c94f68a206b43",
-                "reference": "0c82c96f2a55d8b91bbc7ee6512c94f68a206b43",
-                "shasum": ""
+                "reference": "0c82c96f2a55d8b91bbc7ee6512c94f68a206b43"
             },
             "require": {
                 "php": "^7.2 || ^8.0",
                 "phpstan/phpstan": "^1.6.3"
             },
-            "require-dev": {
-                "nikic/php-parser": "^4.13.0",
-                "php-parallel-lint/php-parallel-lint": "^1.2",
-                "phpstan/phpstan-phpunit": "^1.0",
-                "phpunit/phpunit": "^9.5"
-            },
             "type": "phpstan-extension",
             "extra": {
                 "phpstan": {
                     "includes": [
                         "rules.neon"
                     ]
                 }
             },
             "autoload": {
                 "psr-4": {
                     "PHPStan\\": "src/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "description": "Extra strict and opinionated rules for PHPStan",
-            "support": {
-                "issues": "https://github.com/phpstan/phpstan-strict-rules/issues",
-                "source": "https://github.com/phpstan/phpstan-strict-rules/tree/1.2.3"
-            },
-            "time": "2022-05-04T15:20:40+00:00"
+            "description": "Extra strict and opinionated rules for PHPStan"
         },
         {
             "name": "phpstan/phpstan-symfony",
             "version": "1.2.5",
             "source": {
                 "type": "git",
                 "url": "https://github.com/phpstan/phpstan-symfony.git",
                 "reference": "85be852a17fd5a6b67d4fc6daed21e794f935b2d"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/phpstan/phpstan-symfony/zipball/85be852a17fd5a6b67d4fc6daed21e794f935b2d",
-                "reference": "85be852a17fd5a6b67d4fc6daed21e794f935b2d",
-                "shasum": ""
+                "reference": "85be852a17fd5a6b67d4fc6daed21e794f935b2d"
             },
             "require": {
                 "ext-simplexml": "*",
                 "php": "^7.2 || ^8.0",
                 "phpstan/phpstan": "^1.6"
             },
-            "conflict": {
-                "symfony/framework-bundle": "<3.0"
-            },
-            "require-dev": {
-                "nikic/php-parser": "^4.13.0",
-                "php-parallel-lint/php-parallel-lint": "^1.2",
-                "phpstan/phpstan-phpunit": "^1.0",
-                "phpstan/phpstan-strict-rules": "^1.0",
-                "phpunit/phpunit": "^9.5",
-                "psr/container": "1.0 || 1.1.1",
-                "symfony/config": "^4.2 || ^5.0",
-                "symfony/console": "^4.0 || ^5.0",
-                "symfony/dependency-injection": "^4.0 || ^5.0",
-                "symfony/form": "^4.0 || ^5.0",
-                "symfony/framework-bundle": "^4.4 || ^5.0",
-                "symfony/http-foundation": "^5.1",
-                "symfony/messenger": "^4.2 || ^5.0",
-                "symfony/polyfill-php80": "^1.24",
-                "symfony/serializer": "^4.0 || ^5.0"
-            },
             "type": "phpstan-extension",
             "extra": {
                 "phpstan": {
                     "includes": [
                         "extension.neon",
                         "rules.neon"
                     ]
                 }
             },
             "autoload": {
                 "psr-4": {
                     "PHPStan\\": "src/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Lukáš Unger",
-                    "email": "looky.msc@gmail.com",
-                    "homepage": "https://lookyman.net"
-                }
-            ],
-            "description": "Symfony Framework extensions and rules for PHPStan",
-            "support": {
-                "issues": "https://github.com/phpstan/phpstan-symfony/issues",
-                "source": "https://github.com/phpstan/phpstan-symfony/tree/1.2.5"
-            },
-            "time": "2022-06-10T08:44:35+00:00"
+            "description": "Symfony Framework extensions and rules for PHPStan"
         },
         {
             "name": "symfony/phpunit-bridge",
             "version": "v6.1.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/phpunit-bridge.git",
                 "reference": "092ccc3b364925cd8ed6046bc31dcf3a022bd5a4"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/phpunit-bridge/zipball/092ccc3b364925cd8ed6046bc31dcf3a022bd5a4",
-                "reference": "092ccc3b364925cd8ed6046bc31dcf3a022bd5a4",
-                "shasum": ""
+                "reference": "092ccc3b364925cd8ed6046bc31dcf3a022bd5a4"
             },
             "require": {
                 "php": ">=7.1.3"
             },
-            "conflict": {
-                "phpunit/phpunit": "<7.5|9.1.2"
-            },
-            "require-dev": {
-                "symfony/deprecation-contracts": "^2.1|^3.0",
-                "symfony/error-handler": "^5.4|^6.0"
-            },
-            "suggest": {
-                "symfony/error-handler": "For tracking deprecated interfaces usages at runtime with DebugClassLoader"
-            },
             "bin": [
                 "bin/simple-phpunit"
             ],
             "type": "symfony-bridge",
             "extra": {
                 "thanks": {
                     "name": "phpunit/phpunit",
                     "url": "https://github.com/sebastianbergmann/phpunit"
                 }
             },
             "autoload": {
                 "files": [
                     "bootstrap.php"
                 ],
                 "psr-4": {
                     "Symfony\\Bridge\\PhpUnit\\": ""
                 },
                 "exclude-from-classmap": [
                     "/Tests/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Nicolas Grekas",
-                    "email": "p@tchwork.com"
-                },
-                {
-                    "name": "Symfony Community",
-                    "homepage": "https://symfony.com/contributors"
-                }
-            ],
-            "description": "Provides utilities for PHPUnit, especially user deprecation notices management",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/phpunit-bridge/tree/v6.1.0"
-            },
-            "funding": [
-                {
-                    "url": "https://symfony.com/sponsor",
-                    "type": "custom"
-                },
-                {
-                    "url": "https://github.com/fabpot",
-                    "type": "github"
-                },
-                {
-                    "url": "https://tidelift.com/funding/github/packagist/symfony/symfony",
-                    "type": "tidelift"
-                }
-            ],
-            "time": "2022-04-12T16:22:53+00:00"
+            "description": "Provides utilities for PHPUnit, especially user deprecation notices management"
         }
     ],
     "aliases": [],
     "minimum-stability": "stable",
     "stability-flags": [],
     "prefer-stable": false,
     "prefer-lowest": false,
     "platform": {
         "php": "^7.2.5 || ^8.0"
     },
     "platform-dev": [],
     "platform-overrides": {
         "php": "7.2.5"
     },
     "plugin-api-version": "2.3.0"
 }
```
</details>

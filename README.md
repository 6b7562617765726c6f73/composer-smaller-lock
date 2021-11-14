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
    <summary>Composer's <a href='https://github.com/composer/composer/blob/2.1.12/composer.lock'>composer.lock</a> has 1612 lines, with the plugin the number is reduced to 882.</summary>

```diff
 {
     "_readme": [
         "This file locks the dependencies of your project to a known state",
         "Read more about it at https://getcomposer.org/doc/01-basic-usage.md#installing-dependencies",
         "This file is @generated automatically"
     ],
     "content-hash": "d3dfd8964a34240eba83383a25e2f1fb",
     "packages": [
         {
             "name": "composer/ca-bundle",
             "version": "1.3.1",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/ca-bundle.git",
                 "reference": "4c679186f2aca4ab6a0f1b0b9cf9252decb44d0b"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/ca-bundle/zipball/4c679186f2aca4ab6a0f1b0b9cf9252decb44d0b",
-                "reference": "4c679186f2aca4ab6a0f1b0b9cf9252decb44d0b",
-                "shasum": ""
+                "reference": "4c679186f2aca4ab6a0f1b0b9cf9252decb44d0b"
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
-                "source": "https://github.com/composer/ca-bundle/tree/1.3.1"
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
-            "time": "2021-10-28T20:44:15+00:00"
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
             "name": "composer/semver",
             "version": "3.2.6",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/semver.git",
                 "reference": "83e511e247de329283478496f7a1e114c9517506"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/semver/zipball/83e511e247de329283478496f7a1e114c9517506",
-                "reference": "83e511e247de329283478496f7a1e114c9517506",
-                "shasum": ""
+                "reference": "83e511e247de329283478496f7a1e114c9517506"
             },
             "require": {
                 "php": "^5.3.2 || ^7.0 || ^8.0"
             },
-            "require-dev": {
-                "phpstan/phpstan": "^0.12.54",
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
-                "source": "https://github.com/composer/semver/tree/3.2.6"
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
-            "time": "2021-10-25T11:34:17+00:00"
+            "description": "Semver library that offers utilities, version constraint parsing and validation."
         },
         {
             "name": "composer/spdx-licenses",
             "version": "1.5.5",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/spdx-licenses.git",
                 "reference": "de30328a7af8680efdc03e396aad24befd513200"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/spdx-licenses/zipball/de30328a7af8680efdc03e396aad24befd513200",
-                "reference": "de30328a7af8680efdc03e396aad24befd513200",
-                "shasum": ""
+                "reference": "de30328a7af8680efdc03e396aad24befd513200"
             },
             "require": {
                 "php": "^5.3.2 || ^7.0 || ^8.0"
             },
-            "require-dev": {
-                "phpunit/phpunit": "^4.8.35 || ^5.7 || 6.5 - 7"
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
-                "source": "https://github.com/composer/spdx-licenses/tree/1.5.5"
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
-            "time": "2020-12-03T16:04:16+00:00"
+            "description": "SPDX licenses list and validation library."
         },
         {
             "name": "composer/xdebug-handler",
             "version": "2.0.2",
             "source": {
                 "type": "git",
                 "url": "https://github.com/composer/xdebug-handler.git",
                 "reference": "84674dd3a7575ba617f5a76d7e9e29a7d3891339"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/composer/xdebug-handler/zipball/84674dd3a7575ba617f5a76d7e9e29a7d3891339",
-                "reference": "84674dd3a7575ba617f5a76d7e9e29a7d3891339",
-                "shasum": ""
+                "reference": "84674dd3a7575ba617f5a76d7e9e29a7d3891339"
             },
             "require": {
                 "php": "^5.3.2 || ^7.0 || ^8.0",
                 "psr/log": "^1 || ^2 || ^3"
             },
-            "require-dev": {
-                "phpstan/phpstan": "^0.12.55",
-                "symfony/phpunit-bridge": "^4.2 || ^5"
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
-                "source": "https://github.com/composer/xdebug-handler/tree/2.0.2"
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
-            "time": "2021-07-31T17:03:58+00:00"
+            "description": "Restarts a process without Xdebug."
         },
         {
             "name": "justinrainbow/json-schema",
             "version": "5.2.11",
             "source": {
                 "type": "git",
                 "url": "https://github.com/justinrainbow/json-schema.git",
                 "reference": "2ab6744b7296ded80f8cc4f9509abbff393399aa"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/justinrainbow/json-schema/zipball/2ab6744b7296ded80f8cc4f9509abbff393399aa",
-                "reference": "2ab6744b7296ded80f8cc4f9509abbff393399aa",
-                "shasum": ""
+                "reference": "2ab6744b7296ded80f8cc4f9509abbff393399aa"
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
-                "source": "https://github.com/justinrainbow/json-schema/tree/5.2.11"
-            },
-            "time": "2021-07-22T09:24:00+00:00"
+            "description": "A library to validate a json schema."
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
             "version": "v1.2.1",
             "source": {
                 "type": "git",
                 "url": "https://github.com/reactphp/promise.git",
                 "reference": "eefff597e67ff66b719f8171480add3c91474a1e"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/reactphp/promise/zipball/eefff597e67ff66b719f8171480add3c91474a1e",
-                "reference": "eefff597e67ff66b719f8171480add3c91474a1e",
-                "shasum": ""
+                "reference": "eefff597e67ff66b719f8171480add3c91474a1e"
             },
             "require": {
                 "php": ">=5.3.3"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "1.1-dev"
                 }
             },
             "autoload": {
                 "psr-0": {
                     "React\\Promise": "src/"
                 },
                 "files": [
                     "src/React/Promise/functions_include.php"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Jan Sorgalla",
-                    "email": "jsorgalla@gmail.com"
-                }
-            ],
-            "description": "A lightweight implementation of CommonJS Promises/A for PHP",
-            "support": {
-                "issues": "https://github.com/reactphp/promise/issues",
-                "source": "https://github.com/reactphp/promise/tree/1.0"
-            },
-            "time": "2016-03-07T13:46:50+00:00"
+            "description": "A lightweight implementation of CommonJS Promises/A for PHP"
         },
         {
             "name": "seld/jsonlint",
             "version": "1.8.3",
             "source": {
                 "type": "git",
                 "url": "https://github.com/Seldaek/jsonlint.git",
                 "reference": "9ad6ce79c342fbd44df10ea95511a1b24dee5b57"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/Seldaek/jsonlint/zipball/9ad6ce79c342fbd44df10ea95511a1b24dee5b57",
-                "reference": "9ad6ce79c342fbd44df10ea95511a1b24dee5b57",
-                "shasum": ""
+                "reference": "9ad6ce79c342fbd44df10ea95511a1b24dee5b57"
             },
             "require": {
                 "php": "^5.3 || ^7.0 || ^8.0"
             },
-            "require-dev": {
-                "phpunit/phpunit": "^4.8.35 || ^5.7 || ^6.0"
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
-                "source": "https://github.com/Seldaek/jsonlint/tree/1.8.3"
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
-            "time": "2020-11-11T09:19:24+00:00"
+            "description": "JSON Linter"
         },
         {
             "name": "seld/phar-utils",
             "version": "1.1.2",
             "source": {
                 "type": "git",
                 "url": "https://github.com/Seldaek/phar-utils.git",
                 "reference": "749042a2315705d2dfbbc59234dd9ceb22bf3ff0"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/Seldaek/phar-utils/zipball/749042a2315705d2dfbbc59234dd9ceb22bf3ff0",
-                "reference": "749042a2315705d2dfbbc59234dd9ceb22bf3ff0",
-                "shasum": ""
+                "reference": "749042a2315705d2dfbbc59234dd9ceb22bf3ff0"
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
-                "source": "https://github.com/Seldaek/phar-utils/tree/1.1.2"
-            },
-            "time": "2021-08-19T21:01:38+00:00"
+            "description": "PHAR file format utilities, for when PHP phars you up"
         },
         {
             "name": "symfony/console",
             "version": "v2.8.52",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/console.git",
                 "reference": "cbcf4b5e233af15cd2bbd50dee1ccc9b7927dc12"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/console/zipball/cbcf4b5e233af15cd2bbd50dee1ccc9b7927dc12",
-                "reference": "cbcf4b5e233af15cd2bbd50dee1ccc9b7927dc12",
-                "shasum": ""
+                "reference": "cbcf4b5e233af15cd2bbd50dee1ccc9b7927dc12"
             },
             "require": {
                 "php": ">=5.3.9",
                 "symfony/debug": "^2.7.2|~3.0.0",
                 "symfony/polyfill-mbstring": "~1.0"
             },
-            "require-dev": {
-                "psr/log": "~1.0",
-                "symfony/event-dispatcher": "~2.1|~3.0.0",
-                "symfony/process": "~2.1|~3.0.0"
-            },
-            "suggest": {
-                "psr/log-implementation": "For using the console logger",
-                "symfony/event-dispatcher": "",
-                "symfony/process": ""
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "2.8-dev"
                 }
             },
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
-            "description": "Symfony Console Component",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/console/tree/v2.8.52"
-            },
-            "time": "2018-11-20T15:55:20+00:00"
+            "description": "Symfony Console Component"
         },
         {
             "name": "symfony/debug",
             "version": "v2.8.52",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/debug.git",
                 "reference": "74251c8d50dd3be7c4ce0c7b862497cdc641a5d0"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/debug/zipball/74251c8d50dd3be7c4ce0c7b862497cdc641a5d0",
-                "reference": "74251c8d50dd3be7c4ce0c7b862497cdc641a5d0",
-                "shasum": ""
+                "reference": "74251c8d50dd3be7c4ce0c7b862497cdc641a5d0"
             },
             "require": {
                 "php": ">=5.3.9",
                 "psr/log": "~1.0"
             },
-            "conflict": {
-                "symfony/http-kernel": ">=2.3,<2.3.24|~2.4.0|>=2.5,<2.5.9|>=2.6,<2.6.2"
-            },
-            "require-dev": {
-                "symfony/class-loader": "~2.2|~3.0.0",
-                "symfony/http-kernel": "~2.3.24|~2.5.9|^2.6.2|~3.0.0"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "2.8-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Symfony\\Component\\Debug\\": ""
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
-            "description": "Symfony Debug Component",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/debug/tree/v2.8.50"
-            },
-            "time": "2018-11-11T11:18:13+00:00"
+            "description": "Symfony Debug Component"
         },
         {
             "name": "symfony/filesystem",
             "version": "v2.8.52",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/filesystem.git",
                 "reference": "7ae46872dad09dffb7fe1e93a0937097339d0080"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/filesystem/zipball/7ae46872dad09dffb7fe1e93a0937097339d0080",
-                "reference": "7ae46872dad09dffb7fe1e93a0937097339d0080",
-                "shasum": ""
+                "reference": "7ae46872dad09dffb7fe1e93a0937097339d0080"
             },
             "require": {
                 "php": ">=5.3.9",
                 "symfony/polyfill-ctype": "~1.8"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "2.8-dev"
                 }
             },
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
-            "description": "Symfony Filesystem Component",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/filesystem/tree/v2.8.52"
-            },
-            "time": "2018-11-11T11:18:13+00:00"
+            "description": "Symfony Filesystem Component"
         },
         {
             "name": "symfony/finder",
             "version": "v2.8.52",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/finder.git",
                 "reference": "1444eac52273e345d9b95129bf914639305a9ba4"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/finder/zipball/1444eac52273e345d9b95129bf914639305a9ba4",
-                "reference": "1444eac52273e345d9b95129bf914639305a9ba4",
-                "shasum": ""
+                "reference": "1444eac52273e345d9b95129bf914639305a9ba4"
             },
             "require": {
                 "php": ">=5.3.9"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "2.8-dev"
                 }
             },
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
-            "description": "Symfony Finder Component",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/finder/tree/v2.8.50"
-            },
-            "time": "2018-11-11T11:18:13+00:00"
+            "description": "Symfony Finder Component"
         },
         {
             "name": "symfony/polyfill-ctype",
             "version": "v1.19.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/polyfill-ctype.git",
                 "reference": "aed596913b70fae57be53d86faa2e9ef85a2297b"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/polyfill-ctype/zipball/aed596913b70fae57be53d86faa2e9ef85a2297b",
-                "reference": "aed596913b70fae57be53d86faa2e9ef85a2297b",
-                "shasum": ""
+                "reference": "aed596913b70fae57be53d86faa2e9ef85a2297b"
             },
             "require": {
                 "php": ">=5.3.3"
             },
-            "suggest": {
-                "ext-ctype": "For best performance"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.19-dev"
                 },
                 "thanks": {
                     "name": "symfony/polyfill",
                     "url": "https://github.com/symfony/polyfill"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Symfony\\Polyfill\\Ctype\\": ""
                 },
                 "files": [
                     "bootstrap.php"
                 ]
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
-                "source": "https://github.com/symfony/polyfill-ctype/tree/v1.19.0"
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
-            "time": "2020-10-23T09:01:57+00:00"
+            "description": "Symfony polyfill for ctype functions"
         },
         {
             "name": "symfony/polyfill-mbstring",
             "version": "v1.19.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/polyfill-mbstring.git",
                 "reference": "b5f7b932ee6fa802fc792eabd77c4c88084517ce"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/polyfill-mbstring/zipball/b5f7b932ee6fa802fc792eabd77c4c88084517ce",
-                "reference": "b5f7b932ee6fa802fc792eabd77c4c88084517ce",
-                "shasum": ""
+                "reference": "b5f7b932ee6fa802fc792eabd77c4c88084517ce"
             },
             "require": {
                 "php": ">=5.3.3"
             },
-            "suggest": {
-                "ext-mbstring": "For best performance"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-main": "1.19-dev"
                 },
                 "thanks": {
                     "name": "symfony/polyfill",
                     "url": "https://github.com/symfony/polyfill"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Symfony\\Polyfill\\Mbstring\\": ""
                 },
                 "files": [
                     "bootstrap.php"
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
-                "source": "https://github.com/symfony/polyfill-mbstring/tree/v1.19.0"
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
-            "time": "2020-10-23T09:01:57+00:00"
+            "description": "Symfony polyfill for the Mbstring extension"
         },
         {
             "name": "symfony/process",
             "version": "v2.8.52",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/process.git",
                 "reference": "c3591a09c78639822b0b290d44edb69bf9f05dc8"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/process/zipball/c3591a09c78639822b0b290d44edb69bf9f05dc8",
-                "reference": "c3591a09c78639822b0b290d44edb69bf9f05dc8",
-                "shasum": ""
+                "reference": "c3591a09c78639822b0b290d44edb69bf9f05dc8"
             },
             "require": {
                 "php": ">=5.3.9"
             },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "2.8-dev"
                 }
             },
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
-            "description": "Symfony Process Component",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/process/tree/v2.8.50"
-            },
-            "time": "2018-11-11T11:18:13+00:00"
+            "description": "Symfony Process Component"
         }
     ],
     "packages-dev": [
         {
             "name": "doctrine/instantiator",
             "version": "1.0.5",
             "source": {
                 "type": "git",
                 "url": "https://github.com/doctrine/instantiator.git",
                 "reference": "8e884e78f9f0eb1329e445619e04456e64d8051d"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/doctrine/instantiator/zipball/8e884e78f9f0eb1329e445619e04456e64d8051d",
-                "reference": "8e884e78f9f0eb1329e445619e04456e64d8051d",
-                "shasum": ""
+                "reference": "8e884e78f9f0eb1329e445619e04456e64d8051d"
             },
             "require": {
                 "php": ">=5.3,<8.0-DEV"
             },
-            "require-dev": {
-                "athletic/athletic": "~0.1.8",
-                "ext-pdo": "*",
-                "ext-phar": "*",
-                "phpunit/phpunit": "~4.0",
-                "squizlabs/php_codesniffer": "~2.0"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "1.0.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Doctrine\\Instantiator\\": "src/Doctrine/Instantiator/"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Marco Pivetta",
-                    "email": "ocramius@gmail.com",
-                    "homepage": "http://ocramius.github.com/"
-                }
-            ],
-            "description": "A small, lightweight utility to instantiate objects in PHP without invoking their constructors",
-            "homepage": "https://github.com/doctrine/instantiator",
-            "keywords": [
-                "constructor",
-                "instantiate"
-            ],
-            "support": {
-                "issues": "https://github.com/doctrine/instantiator/issues",
-                "source": "https://github.com/doctrine/instantiator/tree/master"
-            },
-            "time": "2015-06-14T21:17:01+00:00"
+            "description": "A small, lightweight utility to instantiate objects in PHP without invoking their constructors"
         },
         {
             "name": "phpdocumentor/reflection-docblock",
             "version": "2.0.5",
             "source": {
                 "type": "git",
                 "url": "https://github.com/phpDocumentor/ReflectionDocBlock.git",
                 "reference": "e6a969a640b00d8daa3c66518b0405fb41ae0c4b"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/phpDocumentor/ReflectionDocBlock/zipball/e6a969a640b00d8daa3c66518b0405fb41ae0c4b",
-                "reference": "e6a969a640b00d8daa3c66518b0405fb41ae0c4b",
-                "shasum": ""
+                "reference": "e6a969a640b00d8daa3c66518b0405fb41ae0c4b"
             },
             "require": {
                 "php": ">=5.3.3"
             },
-            "require-dev": {
-                "phpunit/phpunit": "~4.0"
-            },
-            "suggest": {
-                "dflydev/markdown": "~1.0",
-                "erusev/parsedown": "~1.0"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "2.0.x-dev"
                 }
             },
             "autoload": {
                 "psr-0": {
                     "phpDocumentor": [
                         "src/"
                     ]
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
-            ],
-            "authors": [
-                {
-                    "name": "Mike van Riel",
-                    "email": "mike.vanriel@naenius.com"
-                }
-            ],
-            "support": {
-                "issues": "https://github.com/phpDocumentor/ReflectionDocBlock/issues",
-                "source": "https://github.com/phpDocumentor/ReflectionDocBlock/tree/release/2.x"
-            },
-            "time": "2016-01-25T08:17:30+00:00"
+            ]
         },
         {
             "name": "phpspec/prophecy",
             "version": "v1.10.3",
             "source": {
                 "type": "git",
                 "url": "https://github.com/phpspec/prophecy.git",
                 "reference": "451c3cd1418cf640de218914901e51b064abb093"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/phpspec/prophecy/zipball/451c3cd1418cf640de218914901e51b064abb093",
-                "reference": "451c3cd1418cf640de218914901e51b064abb093",
-                "shasum": ""
+                "reference": "451c3cd1418cf640de218914901e51b064abb093"
             },
             "require": {
                 "doctrine/instantiator": "^1.0.2",
                 "php": "^5.3|^7.0",
                 "phpdocumentor/reflection-docblock": "^2.0|^3.0.2|^4.0|^5.0",
                 "sebastian/comparator": "^1.2.3|^2.0|^3.0|^4.0",
                 "sebastian/recursion-context": "^1.0|^2.0|^3.0|^4.0"
             },
-            "require-dev": {
-                "phpspec/phpspec": "^2.5 || ^3.2",
-                "phpunit/phpunit": "^4.8.35 || ^5.7 || ^6.5 || ^7.1"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "1.10.x-dev"
                 }
             },
             "autoload": {
                 "psr-4": {
                     "Prophecy\\": "src/Prophecy"
                 }
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "MIT"
             ],
-            "authors": [
-                {
-                    "name": "Konstantin Kudryashov",
-                    "email": "ever.zet@gmail.com",
-                    "homepage": "http://everzet.com"
-                },
-                {
-                    "name": "Marcello Duarte",
-                    "email": "marcello.duarte@gmail.com"
-                }
-            ],
-            "description": "Highly opinionated mocking framework for PHP 5.3+",
-            "homepage": "https://github.com/phpspec/prophecy",
-            "keywords": [
-                "Double",
-                "Dummy",
-                "fake",
-                "mock",
-                "spy",
-                "stub"
-            ],
-            "support": {
-                "issues": "https://github.com/phpspec/prophecy/issues",
-                "source": "https://github.com/phpspec/prophecy/tree/v1.10.3"
-            },
-            "time": "2020-03-05T15:02:03+00:00"
+            "description": "Highly opinionated mocking framework for PHP 5.3+"
         },
         {
             "name": "sebastian/comparator",
             "version": "1.2.4",
             "source": {
                 "type": "git",
                 "url": "https://github.com/sebastianbergmann/comparator.git",
                 "reference": "2b7424b55f5047b47ac6e5ccb20b2aea4011d9be"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/sebastianbergmann/comparator/zipball/2b7424b55f5047b47ac6e5ccb20b2aea4011d9be",
-                "reference": "2b7424b55f5047b47ac6e5ccb20b2aea4011d9be",
-                "shasum": ""
+                "reference": "2b7424b55f5047b47ac6e5ccb20b2aea4011d9be"
             },
             "require": {
                 "php": ">=5.3.3",
                 "sebastian/diff": "~1.2",
                 "sebastian/exporter": "~1.2 || ~2.0"
             },
-            "require-dev": {
-                "phpunit/phpunit": "~4.4"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "1.2.x-dev"
                 }
             },
             "autoload": {
                 "classmap": [
                     "src/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "BSD-3-Clause"
             ],
-            "authors": [
-                {
-                    "name": "Jeff Welch",
-                    "email": "whatthejeff@gmail.com"
-                },
-                {
-                    "name": "Volker Dusch",
-                    "email": "github@wallbash.com"
-                },
-                {
-                    "name": "Bernhard Schussek",
-                    "email": "bschussek@2bepublished.at"
-                },
-                {
-                    "name": "Sebastian Bergmann",
-                    "email": "sebastian@phpunit.de"
-                }
-            ],
-            "description": "Provides the functionality to compare PHP values for equality",
-            "homepage": "http://www.github.com/sebastianbergmann/comparator",
-            "keywords": [
-                "comparator",
-                "compare",
-                "equality"
-            ],
-            "support": {
-                "issues": "https://github.com/sebastianbergmann/comparator/issues",
-                "source": "https://github.com/sebastianbergmann/comparator/tree/1.2"
-            },
-            "time": "2017-01-29T09:50:25+00:00"
+            "description": "Provides the functionality to compare PHP values for equality"
         },
         {
             "name": "sebastian/diff",
             "version": "1.4.3",
             "source": {
                 "type": "git",
                 "url": "https://github.com/sebastianbergmann/diff.git",
                 "reference": "7f066a26a962dbe58ddea9f72a4e82874a3975a4"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/sebastianbergmann/diff/zipball/7f066a26a962dbe58ddea9f72a4e82874a3975a4",
-                "reference": "7f066a26a962dbe58ddea9f72a4e82874a3975a4",
-                "shasum": ""
+                "reference": "7f066a26a962dbe58ddea9f72a4e82874a3975a4"
             },
             "require": {
                 "php": "^5.3.3 || ^7.0"
             },
-            "require-dev": {
-                "phpunit/phpunit": "^4.8.35 || ^5.7 || ^6.0"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "1.4-dev"
                 }
             },
             "autoload": {
                 "classmap": [
                     "src/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "BSD-3-Clause"
             ],
-            "authors": [
-                {
-                    "name": "Kore Nordmann",
-                    "email": "mail@kore-nordmann.de"
-                },
-                {
-                    "name": "Sebastian Bergmann",
-                    "email": "sebastian@phpunit.de"
-                }
-            ],
-            "description": "Diff implementation",
-            "homepage": "https://github.com/sebastianbergmann/diff",
-            "keywords": [
-                "diff"
-            ],
-            "support": {
-                "issues": "https://github.com/sebastianbergmann/diff/issues",
-                "source": "https://github.com/sebastianbergmann/diff/tree/1.4"
-            },
-            "time": "2017-05-22T07:24:03+00:00"
+            "description": "Diff implementation"
         },
         {
             "name": "sebastian/exporter",
             "version": "2.0.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/sebastianbergmann/exporter.git",
                 "reference": "ce474bdd1a34744d7ac5d6aad3a46d48d9bac4c4"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/sebastianbergmann/exporter/zipball/ce474bdd1a34744d7ac5d6aad3a46d48d9bac4c4",
-                "reference": "ce474bdd1a34744d7ac5d6aad3a46d48d9bac4c4",
-                "shasum": ""
+                "reference": "ce474bdd1a34744d7ac5d6aad3a46d48d9bac4c4"
             },
             "require": {
                 "php": ">=5.3.3",
                 "sebastian/recursion-context": "~2.0"
             },
-            "require-dev": {
-                "ext-mbstring": "*",
-                "phpunit/phpunit": "~4.4"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "2.0.x-dev"
                 }
             },
             "autoload": {
                 "classmap": [
                     "src/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "BSD-3-Clause"
             ],
-            "authors": [
-                {
-                    "name": "Jeff Welch",
-                    "email": "whatthejeff@gmail.com"
-                },
-                {
-                    "name": "Volker Dusch",
-                    "email": "github@wallbash.com"
-                },
-                {
-                    "name": "Bernhard Schussek",
-                    "email": "bschussek@2bepublished.at"
-                },
-                {
-                    "name": "Sebastian Bergmann",
-                    "email": "sebastian@phpunit.de"
-                },
-                {
-                    "name": "Adam Harvey",
-                    "email": "aharvey@php.net"
-                }
-            ],
-            "description": "Provides the functionality to export PHP variables for visualization",
-            "homepage": "http://www.github.com/sebastianbergmann/exporter",
-            "keywords": [
-                "export",
-                "exporter"
-            ],
-            "support": {
-                "issues": "https://github.com/sebastianbergmann/exporter/issues",
-                "source": "https://github.com/sebastianbergmann/exporter/tree/master"
-            },
-            "time": "2016-11-19T08:54:04+00:00"
+            "description": "Provides the functionality to export PHP variables for visualization"
         },
         {
             "name": "sebastian/recursion-context",
             "version": "2.0.0",
             "source": {
                 "type": "git",
                 "url": "https://github.com/sebastianbergmann/recursion-context.git",
                 "reference": "2c3ba150cbec723aa057506e73a8d33bdb286c9a"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/sebastianbergmann/recursion-context/zipball/2c3ba150cbec723aa057506e73a8d33bdb286c9a",
-                "reference": "2c3ba150cbec723aa057506e73a8d33bdb286c9a",
-                "shasum": ""
+                "reference": "2c3ba150cbec723aa057506e73a8d33bdb286c9a"
             },
             "require": {
                 "php": ">=5.3.3"
             },
-            "require-dev": {
-                "phpunit/phpunit": "~4.4"
-            },
             "type": "library",
             "extra": {
                 "branch-alias": {
                     "dev-master": "2.0.x-dev"
                 }
             },
             "autoload": {
                 "classmap": [
                     "src/"
                 ]
             },
-            "notification-url": "https://packagist.org/downloads/",
             "license": [
                 "BSD-3-Clause"
             ],
-            "authors": [
-                {
-                    "name": "Jeff Welch",
-                    "email": "whatthejeff@gmail.com"
-                },
-                {
-                    "name": "Sebastian Bergmann",
-                    "email": "sebastian@phpunit.de"
-                },
-                {
-                    "name": "Adam Harvey",
-                    "email": "aharvey@php.net"
-                }
-            ],
-            "description": "Provides functionality to recursively process PHP variables",
-            "homepage": "http://www.github.com/sebastianbergmann/recursion-context",
-            "support": {
-                "issues": "https://github.com/sebastianbergmann/recursion-context/issues",
-                "source": "https://github.com/sebastianbergmann/recursion-context/tree/master"
-            },
-            "time": "2016-11-19T07:33:16+00:00"
+            "description": "Provides functionality to recursively process PHP variables"
         },
         {
             "name": "symfony/phpunit-bridge",
             "version": "v4.2.12",
             "source": {
                 "type": "git",
                 "url": "https://github.com/symfony/phpunit-bridge.git",
                 "reference": "80f9ffa6afcc27c7b00e8b8446b1d5d48d94bae7"
             },
             "dist": {
                 "type": "zip",
                 "url": "https://api.github.com/repos/symfony/phpunit-bridge/zipball/80f9ffa6afcc27c7b00e8b8446b1d5d48d94bae7",
-                "reference": "80f9ffa6afcc27c7b00e8b8446b1d5d48d94bae7",
-                "shasum": ""
+                "reference": "80f9ffa6afcc27c7b00e8b8446b1d5d48d94bae7"
             },
             "require": {
                 "php": ">=5.3.3"
             },
-            "conflict": {
-                "phpunit/phpunit": "<4.8.35|<5.4.3,>=5.0"
-            },
-            "suggest": {
-                "symfony/debug": "For tracking deprecated interfaces usages at runtime with DebugClassLoader"
-            },
             "bin": [
                 "bin/simple-phpunit"
             ],
             "type": "symfony-bridge",
             "extra": {
                 "branch-alias": {
                     "dev-master": "4.2-dev"
                 },
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
-            "description": "Symfony PHPUnit Bridge",
-            "homepage": "https://symfony.com",
-            "support": {
-                "source": "https://github.com/symfony/phpunit-bridge/tree/4.2"
-            },
-            "time": "2019-07-05T06:33:37+00:00"
+            "description": "Symfony PHPUnit Bridge"
         }
     ],
     "aliases": [],
     "minimum-stability": "stable",
     "stability-flags": [],
     "prefer-stable": false,
     "prefer-lowest": false,
     "platform": {
         "php": "^5.3.2 || ^7.0 || ^8.0"
     },
     "platform-dev": [],
     "platform-overrides": {
         "php": "5.3.9"
     },
     "plugin-api-version": "2.1.0"
 }
```
</details>

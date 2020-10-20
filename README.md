# Implied dependencies
Package that prevents installing superfluous polyfills. It’s a public repository so it can be published in packagist.
It’s probably not useful for anybody outside of InterNations.

## How it works
The package requires a particular PHP version and a particular set of PHP extensions and specifies a `replace` section
for polyfills that no longer need to be installed. This `replace` section prevents the installation of said
dependencies.

## Versioning
 Keep version of the metapackage in sync with PHP’s major/minor target version. So `internations/php-implied: 7.4.0`
 targets `php: >=7.4.0 && <7.5`

## Changing the package
 * Add a new element to the `replace` section
 * Run `composer validate`
 * Tag a new tag from master to automatically release a new packagist version

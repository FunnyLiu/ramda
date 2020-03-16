
# 源码分析

## 文件结构

``` bash
/Users/liufang/openSource/FunnyLiu/ramda
├── lib
|  ├── bench
|  |  ├── concat.bench.js
|  |  ├── curry.bench.js
|  |  ├── each.bench.js
|  |  ├── either.bench.js
|  |  ├── filter-where.bench.js
|  |  ├── filter.bench.js
|  |  ├── find-where.bench.js
|  |  ├── find.bench.js
|  |  ├── findIndex-where.bench.js
|  |  ├── findIndex.bench.js
|  |  ├── includes.bench.js
|  |  ├── indexof.bench.js
|  |  ├── map.bench.js
|  |  ├── maxWith.bench.js
|  |  ├── propEq.bench.js
|  |  ├── reduce.bench.js
|  |  └── uniq.bench.js
|  └── sauce
|     ├── android.js
|     ├── apple.js
|     ├── browsers.js
|     ├── conf.js
|     ├── ie8-shim.js
|     ├── ios.js
|     ├── linux.js
|     ├── mocharun.js
|     ├── server.js
|     └── windows.js
├── source
|  ├── F.js
|  ├── T.js
|  ├── __.js
|  ├── add.js
|  ├── addIndex.js
|  ├── adjust.js
|  ├── all.js
|  ├── allPass.js
|  ├── always.js
|  ├── and.js
|  ├── andThen.js
|  ├── any.js
|  ├── anyPass.js
|  ├── ap.js
|  ├── aperture.js
|  ├── append.js
|  ├── apply.js
|  ├── applySpec.js
|  ├── applyTo.js
|  ├── ascend.js
|  ├── assoc.js
|  ├── assocPath.js
|  ├── binary.js
|  ├── bind.js
|  ├── both.js
|  ├── call.js
|  ├── chain.js
|  ├── clamp.js
|  ├── clone.js
|  ├── comparator.js
|  ├── complement.js
|  ├── compose.js
|  ├── composeWith.js
|  ├── concat.js
|  ├── cond.js
|  ├── construct.js
|  ├── constructN.js
|  ├── converge.js
|  ├── countBy.js
|  ├── curry.js
|  ├── curryN.js
|  ├── dec.js
|  ├── defaultTo.js
|  ├── descend.js
|  ├── difference.js
|  ├── differenceWith.js
|  ├── dissoc.js
|  ├── dissocPath.js
|  ├── divide.js
|  ├── drop.js
|  ├── dropLast.js
|  ├── dropLastWhile.js
|  ├── dropRepeats.js
|  ├── dropRepeatsWith.js
|  ├── dropWhile.js
|  ├── either.js
|  ├── empty.js
|  ├── endsWith.js
|  ├── eqBy.js
|  ├── eqProps.js
|  ├── equals.js
|  ├── evolve.js
|  ├── filter.js
|  ├── find.js
|  ├── findIndex.js
|  ├── findLast.js
|  ├── findLastIndex.js
|  ├── flatten.js
|  ├── flip.js
|  ├── forEach.js
|  ├── forEachObjIndexed.js
|  ├── fromPairs.js
|  ├── groupBy.js
|  ├── groupWith.js
|  ├── gt.js
|  ├── gte.js
|  ├── has.js
|  ├── hasIn.js
|  ├── hasPath.js
|  ├── head.js
|  ├── identical.js
|  ├── identity.js
|  ├── ifElse.js
|  ├── inc.js
|  ├── includes.js
|  ├── index.js
|  ├── indexBy.js
|  ├── indexOf.js
|  ├── init.js
|  ├── innerJoin.js
|  ├── insert.js
|  ├── insertAll.js
|  ├── internal
|  |  ├── _Set.js
|  |  ├── _aperture.js
|  |  ├── _arity.js
|  |  ├── _arrayFromIterator.js
|  |  ├── _assertPromise.js
|  |  ├── _checkForMethod.js
|  |  ├── _clone.js
|  |  ├── _cloneRegExp.js
|  |  ├── _complement.js
|  |  ├── _concat.js
|  |  ├── _createPartialApplicator.js
|  |  ├── _curry1.js
|  |  ├── _curry2.js
|  |  ├── _curry3.js
|  |  ├── _curryN.js
|  |  ├── _dispatchable.js
|  |  ├── _dropLast.js
|  |  ├── _dropLastWhile.js
|  |  ├── _equals.js
|  |  ├── _filter.js
|  |  ├── _flatCat.js
|  |  ├── _forceReduced.js
|  |  ├── _functionName.js
|  |  ├── _functionsWith.js
|  |  ├── _has.js
|  |  ├── _identity.js
|  |  ├── _includes.js
|  |  ├── _includesWith.js
|  |  ├── _indexOf.js
|  |  ├── _isArguments.js
|  |  ├── _isArray.js
|  |  ├── _isArrayLike.js
|  |  ├── _isFunction.js
|  |  ├── _isInteger.js
|  |  ├── _isNumber.js
|  |  ├── _isObject.js
|  |  ├── _isPlaceholder.js
|  |  ├── _isRegExp.js
|  |  ├── _isString.js
|  |  ├── _isTransformer.js
|  |  ├── _isTypedArray.js
|  |  ├── _makeFlat.js
|  |  ├── _map.js
|  |  ├── _objectAssign.js
|  |  ├── _objectIs.js
|  |  ├── _of.js
|  |  ├── _pipe.js
|  |  ├── _pipeP.js
|  |  ├── _quote.js
|  |  ├── _reduce.js
|  |  ├── _reduced.js
|  |  ├── _stepCat.js
|  |  ├── _toISOString.js
|  |  ├── _toString.js
|  |  ├── _xall.js
|  |  ├── _xany.js
|  |  ├── _xaperture.js
|  |  ├── _xchain.js
|  |  ├── _xdrop.js
|  |  ├── _xdropLast.js
|  |  ├── _xdropLastWhile.js
|  |  ├── _xdropRepeatsWith.js
|  |  ├── _xdropWhile.js
|  |  ├── _xfBase.js
|  |  ├── _xfilter.js
|  |  ├── _xfind.js
|  |  ├── _xfindIndex.js
|  |  ├── _xfindLast.js
|  |  ├── _xfindLastIndex.js
|  |  ├── _xmap.js
|  |  ├── _xreduceBy.js
|  |  ├── _xtake.js
|  |  ├── _xtakeWhile.js
|  |  ├── _xtap.js
|  |  └── _xwrap.js
|  ├── intersection.js
|  ├── intersperse.js
|  ├── into.js
|  ├── invert.js
|  ├── invertObj.js
|  ├── invoker.js
|  ├── is.js
|  ├── isEmpty.js
|  ├── isNil.js
|  ├── join.js
|  ├── juxt.js
|  ├── keys.js
|  ├── keysIn.js
|  ├── last.js
|  ├── lastIndexOf.js
|  ├── length.js
|  ├── lens.js
|  ├── lensIndex.js
|  ├── lensPath.js
|  ├── lensProp.js
|  ├── lift.js
|  ├── liftN.js
|  ├── lt.js
|  ├── lte.js
|  ├── map.js
|  ├── mapAccum.js
|  ├── mapAccumRight.js
|  ├── mapObjIndexed.js
|  ├── match.js
|  ├── mathMod.js
|  ├── max.js
|  ├── maxBy.js
|  ├── mean.js
|  ├── median.js
|  ├── memoizeWith.js
|  ├── mergeAll.js
|  ├── mergeDeepLeft.js
|  ├── mergeDeepRight.js
|  ├── mergeDeepWith.js
|  ├── mergeDeepWithKey.js
|  ├── mergeLeft.js
|  ├── mergeRight.js
|  ├── mergeWith.js
|  ├── mergeWithKey.js
|  ├── min.js
|  ├── minBy.js
|  ├── modulo.js
|  ├── move.js
|  ├── multiply.js
|  ├── nAry.js
|  ├── negate.js
|  ├── none.js
|  ├── not.js
|  ├── nth.js
|  ├── nthArg.js
|  ├── o.js
|  ├── objOf.js
|  ├── of.js
|  ├── omit.js
|  ├── on.js
|  ├── once.js
|  ├── or.js
|  ├── otherwise.js
|  ├── over.js
|  ├── pair.js
|  ├── partial.js
|  ├── partialRight.js
|  ├── partition.js
|  ├── path.js
|  ├── pathEq.js
|  ├── pathOr.js
|  ├── pathSatisfies.js
|  ├── paths.js
|  ├── pick.js
|  ├── pickAll.js
|  ├── pickBy.js
|  ├── pipe.js
|  ├── pipeWith.js
|  ├── pluck.js
|  ├── prepend.js
|  ├── product.js
|  ├── project.js
|  ├── prop.js
|  ├── propEq.js
|  ├── propIs.js
|  ├── propOr.js
|  ├── propSatisfies.js
|  ├── props.js
|  ├── range.js
|  ├── reduce.js
|  ├── reduceBy.js
|  ├── reduceRight.js
|  ├── reduceWhile.js
|  ├── reduced.js
|  ├── reject.js
|  ├── remove.js
|  ├── repeat.js
|  ├── replace.js
|  ├── reverse.js
|  ├── scan.js
|  ├── sequence.js
|  ├── set.js
|  ├── slice.js
|  ├── sort.js
|  ├── sortBy.js
|  ├── sortWith.js
|  ├── split.js
|  ├── splitAt.js
|  ├── splitEvery.js
|  ├── splitWhen.js
|  ├── splitWhenever.js
|  ├── startsWith.js
|  ├── subtract.js
|  ├── sum.js
|  ├── symmetricDifference.js
|  ├── symmetricDifferenceWith.js
|  ├── tail.js
|  ├── take.js
|  ├── takeLast.js
|  ├── takeLastWhile.js
|  ├── takeWhile.js
|  ├── tap.js
|  ├── test.js
|  ├── thunkify.js
|  ├── times.js
|  ├── toLower.js
|  ├── toPairs.js
|  ├── toPairsIn.js
|  ├── toString.js
|  ├── toUpper.js
|  ├── transduce.js
|  ├── transpose.js
|  ├── traverse.js
|  ├── trim.js
|  ├── tryCatch.js
|  ├── type.js
|  ├── unapply.js
|  ├── unary.js
|  ├── uncurryN.js
|  ├── unfold.js
|  ├── union.js
|  ├── unionWith.js
|  ├── uniq.js
|  ├── uniqBy.js
|  ├── uniqWith.js
|  ├── unless.js
|  ├── unnest.js
|  ├── until.js
|  ├── update.js
|  ├── useWith.js
|  ├── values.js
|  ├── valuesIn.js
|  ├── view.js
|  ├── when.js
|  ├── where.js
|  ├── whereAny.js
|  ├── whereEq.js
|  ├── without.js
|  ├── xor.js
|  ├── xprod.js
|  ├── zip.js
|  ├── zipObj.js
|  └── zipWith.js
└── testem.json

directory: 11 file: 641

ignored: directory (1)

```

## 外部模块依赖

请在： http://npm.broofa.com?q=ramda 查看

## 内部模块依赖

![img](./inner.svg)
  



Ramda
=============

A practical functional library for JavaScript programmers.

[![Build Status](https://travis-ci.org/ramda/ramda.svg?branch=master)](https://travis-ci.org/ramda/ramda)
[![npm module](https://badge.fury.io/js/ramda.svg)](https://www.npmjs.org/package/ramda)
[![dependencies](https://david-dm.org/ramda/ramda.svg)](https://david-dm.org/ramda/ramda)
[![Gitter](https://badges.gitter.im/Join_Chat.svg)](https://gitter.im/ramda/ramda?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)



Why Ramda?
----------

<img src="https://ramdajs.com/ramdaFilled_200x235.png" 
     width="170" height="190" align="right" hspace="12" />

There are already several excellent libraries with a functional flavor. Typically, they are meant to be general-purpose toolkits, suitable for working in multiple paradigms. Ramda has a more focused goal. We wanted a library designed specifically for a functional programming style, one that makes it easy to create functional pipelines, one that never mutates user data. 



What's Different?
-----------------

The primary distinguishing features of Ramda are:

* Ramda emphasizes a purer functional style. Immutability and side-effect free functions 
  are at the heart of its design philosophy. This can help you get the job done with simple, 
  elegant code.

* Ramda functions are automatically curried. This allows you to easily build up new functions 
  from old ones simply by not supplying the final parameters.

* The parameters to Ramda functions are arranged to make it convenient for currying. The data 
  to be operated on is generally supplied last.

The last two points together make it very easy to build functions as sequences of simpler functions, each of which transforms the data and passes it along to the next. Ramda is designed to support this style of coding.



Introductions
-------------

* [Introducing Ramda](http://buzzdecafe.github.io/code/2014/05/16/introducing-ramda) by Buzz de Cafe
* [Why Ramda?](http://fr.umio.us/why-ramda/) by Scott Sauyet
* [Favoring Curry](http://fr.umio.us/favoring-curry/) by Scott Sauyet
* [Why Curry Helps](https://hughfdjackson.com/javascript/why-curry-helps/) by Hugh Jackson
* [Hey Underscore, You're Doing It Wrong!](https://www.youtube.com/watch?v=m3svKOdZijA&app=desktop) by Brian Lonsdorf
* [Thinking in Ramda](https://randycoulman.com/blog/categories/thinking-in-ramda) by Randy Coulman



Philosophy
----------
Using Ramda should feel much like just using JavaScript.
It is practical, functional JavaScript. We're not introducing
lambda expressions in strings, we're not borrowing consed 
lists, we're not porting over all of the Clojure functions.

Our basic data structures are plain JavaScript objects, and our
usual collections are JavaScript arrays. We also keep other
native features of JavaScript, such as functions as objects
with properties.

Functional programming is in good part about immutable objects and 
side-effect free functions. While Ramda does not *enforce* this, it
enables such style to be as frictionless as possible.

We aim for an implementation both clean and elegant, but the API is king.
We sacrifice a great deal of implementation elegance for even a slightly
cleaner API.

Last but not least, Ramda strives for performance. A reliable and quick
implementation wins over any notions of functional purity.



Installation
------------

To use with node:

```bash
$ npm install ramda
```

Then in the console:

```javascript
const R = require('ramda');
```

To use directly in the browser:

```html
<script src="path/to/yourCopyOf/ramda.js"></script>
```

or the minified version:

```html
<script src="path/to/yourCopyOf/ramda.min.js"></script>
```

or from a CDN, either cdnjs:

```html
<script src="//cdnjs.cloudflare.com/ajax/libs/ramda/0.25.0/ramda.min.js"></script>
```

or one of the below links from [jsDelivr](http://jsdelivr.com):

```html
<script src="//cdn.jsdelivr.net/npm/ramda@0.25.0/dist/ramda.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/ramda@0.25/dist/ramda.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/ramda@latest/dist/ramda.min.js"></script>
```

(note that using `latest` is taking a significant risk that ramda API changes could break your code.)

These script tags add the variable `R` on the browser's global scope.

Or you can inject ramda into virtually any unsuspecting website using [the bookmarklet](https://github.com/ramda/ramda/blob/master/BOOKMARKLET.md).

**Note for versions > 0.25**
Ramda versions > 0.25 don't have a default export.
So instead of `import R from 'ramda';`, one has to use `import * as R from 'ramda';`
Or better yet, import only the required functions via `import { functionName } from 'ramda';`

### Build

`npm run build` creates `es`, `src` directories and updates both __dist/ramda.js__ and __dist/ramda.min.js__

#### Partial Builds

It is possible to build Ramda with a subset of the functionality to reduce its file size. Ramda's build system supports this with command line flags. For example if you're using `R.compose`, `R.reduce`, and `R.filter` you can create a partial build with:

    npm run --silent partial-build compose reduce filter > dist/ramda.custom.js

This requires having Node/io.js installed and ramda's dependencies installed (just use `npm install` before running partial build). 

### Install specific functions

[Install individual functions](https://bitsrc.io/ramda/ramda) with bit, npm and yarn without installing the whole library.

Documentation
-------------

Please review the [API documentation](https://ramdajs.com/docs/).

Also available is our [Cookbook](https://github.com/ramda/ramda/wiki/Cookbook) of functions built from Ramda that you may find useful.


The Name
--------

Ok, so we like sheep.  That's all.  It's a short name, not already 
taken.  It could as easily have been `eweda`, but then we would be 
forced to say _eweda lamb!_, and no one wants that.  For non-English 
speakers, lambs are baby sheep, ewes are female sheep, and rams are male 
sheep.  So perhaps ramda is a grown-up lambda... but probably not.




Running The Test Suite
----------------------

**Console:**

To run the test suite from the console, you need to have `mocha` installed:

    npm install -g mocha

Then from the root of the project, you can just call

    mocha

Alternately, if you've installed the dependencies, via:

    npm install

then you can run the tests (and get detailed output) by running:

    npm test

**Browser:**

You can use [testem](https://github.com/airportyh/testem) to
test across different browsers (or even headlessly), with livereloading of
tests. Install testem (`npm install -g testem`) and run `testem`. Open the
link provided in your browser and you will see the results in your terminal.

If you have _PhantomJS_ installed, you can run `testem -l phantomjs` to run the
tests completely headlessly.


Usage
-----------------

For `v0.25` and up, import the whole library or pick ES modules directly from the library:

```js
import * as R from 'ramda'

const {identity} = R
R.map(identity, [1, 2, 3])
```

Destructuring imports from ramda *does not necessarily prevent importing the entire library*. You can manually cherry-pick methods like the following, which would only grab the parts necessary for `identity` to work:

```js
import identity from 'ramda/src/identity'

identity()
```

Manually cherry picking methods is cumbersome, however. Most bundlers like Webpack and Rollup offer tree-shaking as a way to drop unused Ramda code and reduce bundle size, but their performance varies, discussed [here](https://github.com/scabbiaza/ramda-webpack-tree-shaking-examples). Here is a summary of the optimal setup based on what technology you are using:

1. Webpack + Babel - use [`babel-plugin-ramda`](https://github.com/megawac/babel-plugin-ramda) to automatically cherry pick methods. Discussion [here](https://www.andrewsouthpaw.com/ramda-webpack-and-tree-shaking/), example [here](https://github.com/AndrewSouthpaw/ramda-webpack-tree-shaking-examples/blob/master/07-webpack-babel-plugin-ramda/package.json)
1. Webpack only - use `UglifyJS` plugin for treeshaking along with the `ModuleConcatenationPlugin`. Discussion [here](https://github.com/ramda/ramda/issues/2355), with an example setup [here](https://github.com/scabbiaza/ramda-webpack-tree-shaking-examples/blob/master/06-webpack-scope-hoisted/webpack.config.js)
1. Rollup - does a fine job properly treeshaking, no special work needed; example [here](https://github.com/scabbiaza/ramda-webpack-tree-shaking-examples/blob/master/07-rollup-ramda-tree-shaking/rollup.config.js)


Typings
-----------------

- [TypeScript](https://www.npmjs.com/package/@types/ramda)
- [Flow](https://github.com/flowtype/flow-typed/tree/master/definitions/npm/ramda_v0.x.x)




Translations
-----------------

- [Chinese(中文)](http://ramda.cn/)
- [Ukrainian(Українська)](https://github.com/ivanzusko/ramda)
- [Portuguese(BR)](https://github.com/renansj/ramda)
- [Russian(Русский)](https://github.com/Guck111/ramda)
- [Spanish(ES)](https://github.com/wirecobweb/ramda)




Acknowledgements
-----------------

Thanks to [J. C. Phillipps](http://www.jcphillipps.com) for the Ramda logo.
Ramda logo artwork &copy; 2014 J. C. Phillipps. Licensed Creative Commons 
[CC BY-NC-SA 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/).

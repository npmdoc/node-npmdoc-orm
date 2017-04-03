# api documentation for  [orm (v3.2.3)](http://dresende.github.io/node-orm2)  [![npm package](https://img.shields.io/npm/v/npmdoc-orm.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-orm) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-orm.svg)](https://travis-ci.org/npmdoc/node-npmdoc-orm)
#### NodeJS Object-relational mapping

[![NPM](https://nodei.co/npm/orm.png?downloads=true)](https://www.npmjs.com/package/orm)

[![apidoc](https://npmdoc.github.io/node-npmdoc-orm/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-orm_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-orm/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-orm/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-orm/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "analyse": false,
    "author": {
        "name": "Diogo Resende",
        "email": "dresende@thinkdigital.pt"
    },
    "bugs": {
        "url": "https://github.com/dresende/node-orm2/issues"
    },
    "contributors": [
        {
            "name": "Bramus Van Damme",
            "email": "bramus@bram.us"
        },
        {
            "name": "Lorien Gamaroff",
            "email": "lorien@gamaroff.org"
        },
        {
            "name": "preslavrachev"
        },
        {
            "name": "Chris Cowan",
            "email": "me@chriscowan.us"
        },
        {
            "name": "Paul Dixon",
            "email": "paul.dixon@mintbridge.co.uk"
        },
        {
            "name": "David Kosub"
        },
        {
            "name": "Arek W",
            "email": "arek01@gmail.com"
        },
        {
            "name": "Joseph Gilley",
            "email": "joe.gilley@gmail.com"
        },
        {
            "name": "Benjamin Pannell",
            "email": "admin@sierrasoftworks.com"
        }
    ],
    "dependencies": {
        "async": "2.1.4",
        "enforce": "0.1.7",
        "hat": "0.0.3",
        "lodash": "4.17.2",
        "path-is-absolute": "1.0.1",
        "sql-ddl-sync": "0.3.12",
        "sql-query": "0.1.26"
    },
    "description": "NodeJS Object-relational mapping",
    "devDependencies": {
        "glob": "7.1.1",
        "mocha": "3.2.0",
        "mongodb": "1.4.10",
        "mysql": "2.12.0",
        "pg": "6.1.0",
        "should": "11.1.1",
        "sqlite3": "3.1.8"
    },
    "directories": {},
    "dist": {
        "shasum": "53ce621d84b026ad8fdb5afd918f60aff1710f20",
        "tarball": "https://registry.npmjs.org/orm/-/orm-3.2.3.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "25de119e1f47b532626c1591257bbd8bf5d72505",
    "homepage": "http://dresende.github.io/node-orm2",
    "keywords": [
        "orm",
        "odm",
        "database",
        "mysql",
        "postgres",
        "redshift",
        "sqlite",
        "mongodb"
    ],
    "license": "MIT",
    "main": "./lib/ORM",
    "maintainers": [
        {
            "name": "dresende",
            "email": "dresende@thinkdigital.pt"
        },
        {
            "name": "dxg",
            "email": "arek01@gmail.com"
        }
    ],
    "name": "orm",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/dresende/node-orm2.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "3.2.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module orm](#apidoc.module.orm)
1.  [function <span class="apidocSignatureSpan">orm.</span>Error (message, code, extras)](#apidoc.element.orm.Error)
1.  [function <span class="apidocSignatureSpan">orm.</span>Text (data)](#apidoc.element.orm.Text)
1.  [function <span class="apidocSignatureSpan">orm.</span>addAdapter (name, constructor)](#apidoc.element.orm.addAdapter)
1.  [function <span class="apidocSignatureSpan">orm.</span>between (a, b)](#apidoc.element.orm.between)
1.  [function <span class="apidocSignatureSpan">orm.</span>connect (opts, cb)](#apidoc.element.orm.connect)
1.  [function <span class="apidocSignatureSpan">orm.</span>enforce.Enforce (options)](#apidoc.element.orm.enforce.Enforce)
1.  [function <span class="apidocSignatureSpan">orm.</span>enforce.Validator (validate)](#apidoc.element.orm.enforce.Validator)
1.  [function <span class="apidocSignatureSpan">orm.</span>eq (v)](#apidoc.element.orm.eq)
1.  [function <span class="apidocSignatureSpan">orm.</span>express ()](#apidoc.element.orm.express)
1.  [function <span class="apidocSignatureSpan">orm.</span>gt (v)](#apidoc.element.orm.gt)
1.  [function <span class="apidocSignatureSpan">orm.</span>gte (v)](#apidoc.element.orm.gte)
1.  [function <span class="apidocSignatureSpan">orm.</span>like (expr)](#apidoc.element.orm.like)
1.  [function <span class="apidocSignatureSpan">orm.</span>lt (v)](#apidoc.element.orm.lt)
1.  [function <span class="apidocSignatureSpan">orm.</span>lte (v)](#apidoc.element.orm.lte)
1.  [function <span class="apidocSignatureSpan">orm.</span>ne (v)](#apidoc.element.orm.ne)
1.  [function <span class="apidocSignatureSpan">orm.</span>not_between (a, b)](#apidoc.element.orm.not_between)
1.  [function <span class="apidocSignatureSpan">orm.</span>not_in (v)](#apidoc.element.orm.not_in)
1.  [function <span class="apidocSignatureSpan">orm.</span>not_like (expr)](#apidoc.element.orm.not_like)
1.  [function <span class="apidocSignatureSpan">orm.</span>use (connection, proto, opts, cb)](#apidoc.element.orm.use)
1.  object <span class="apidocSignatureSpan">orm.</span>Adapters
1.  object <span class="apidocSignatureSpan">orm.</span>Debug
1.  object <span class="apidocSignatureSpan">orm.</span>Error.prototype
1.  object <span class="apidocSignatureSpan">orm.</span>ErrorCodes
1.  object <span class="apidocSignatureSpan">orm.</span>Hook
1.  object <span class="apidocSignatureSpan">orm.</span>Instance
1.  object <span class="apidocSignatureSpan">orm.</span>LazyLoad
1.  object <span class="apidocSignatureSpan">orm.</span>Model
1.  object <span class="apidocSignatureSpan">orm.</span>Promise
1.  object <span class="apidocSignatureSpan">orm.</span>Property
1.  object <span class="apidocSignatureSpan">orm.</span>Settings
1.  object <span class="apidocSignatureSpan">orm.</span>Utilities
1.  object <span class="apidocSignatureSpan">orm.</span>enforce
1.  object <span class="apidocSignatureSpan">orm.</span>enforce.Enforce.prototype
1.  object <span class="apidocSignatureSpan">orm.</span>enforce.Validator.prototype
1.  object <span class="apidocSignatureSpan">orm.</span>enforce.lists
1.  object <span class="apidocSignatureSpan">orm.</span>enforce.patterns
1.  object <span class="apidocSignatureSpan">orm.</span>enforce.ranges
1.  object <span class="apidocSignatureSpan">orm.</span>enforce.security
1.  object <span class="apidocSignatureSpan">orm.</span>settings
1.  object <span class="apidocSignatureSpan">orm.</span>singleton
1.  object <span class="apidocSignatureSpan">orm.</span>validators

#### [module orm.Adapters](#apidoc.module.orm.Adapters)
1.  [function <span class="apidocSignatureSpan">orm.Adapters.</span>add (name, constructor)](#apidoc.element.orm.Adapters.add)
1.  [function <span class="apidocSignatureSpan">orm.Adapters.</span>get (name)](#apidoc.element.orm.Adapters.get)

#### [module orm.Debug](#apidoc.module.orm.Debug)
1.  [function <span class="apidocSignatureSpan">orm.Debug.</span>sql (driver, sql)](#apidoc.element.orm.Debug.sql)

#### [module orm.Error](#apidoc.module.orm.Error)
1.  [function <span class="apidocSignatureSpan">orm.</span>Error (message, code, extras)](#apidoc.element.orm.Error.Error)
1.  object <span class="apidocSignatureSpan">orm.Error.</span>codes

#### [module orm.Error.prototype](#apidoc.module.orm.Error.prototype)
1.  [function <span class="apidocSignatureSpan">orm.Error.prototype.</span>constructor (message, code, extras)](#apidoc.element.orm.Error.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">orm.Error.prototype.</span>toString ()](#apidoc.element.orm.Error.prototype.toString)
1.  string <span class="apidocSignatureSpan">orm.Error.prototype.</span>name

#### [module orm.Hook](#apidoc.module.orm.Hook)
1.  [function <span class="apidocSignatureSpan">orm.Hook.</span>trigger ()](#apidoc.element.orm.Hook.trigger)
1.  [function <span class="apidocSignatureSpan">orm.Hook.</span>wait ()](#apidoc.element.orm.Hook.wait)

#### [module orm.Instance](#apidoc.module.orm.Instance)
1.  [function <span class="apidocSignatureSpan">orm.</span>Instance (Model, opts)](#apidoc.element.orm.Instance.Instance)

#### [module orm.LazyLoad](#apidoc.module.orm.LazyLoad)
1.  [function <span class="apidocSignatureSpan">orm.LazyLoad.</span>extend (Instance, Model, properties)](#apidoc.element.orm.LazyLoad.extend)

#### [module orm.Model](#apidoc.module.orm.Model)
1.  [function <span class="apidocSignatureSpan">orm.</span>Model (opts)](#apidoc.element.orm.Model.Model)

#### [module orm.Promise](#apidoc.module.orm.Promise)
1.  [function <span class="apidocSignatureSpan">orm.</span>Promise (opts)](#apidoc.element.orm.Promise.Promise)

#### [module orm.Property](#apidoc.module.orm.Property)
1.  [function <span class="apidocSignatureSpan">orm.Property.</span>normalize (opts)](#apidoc.element.orm.Property.normalize)

#### [module orm.Settings](#apidoc.module.orm.Settings)
1.  [function <span class="apidocSignatureSpan">orm.Settings.</span>Container (settings)](#apidoc.element.orm.Settings.Container)
1.  [function <span class="apidocSignatureSpan">orm.Settings.</span>defaults ()](#apidoc.element.orm.Settings.defaults)

#### [module orm.Utilities](#apidoc.module.orm.Utilities)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>checkConditions (conditions, one_associations)](#apidoc.element.orm.Utilities.checkConditions)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>convertPropToJoinKeyProp (props, opts)](#apidoc.element.orm.Utilities.convertPropToJoinKeyProp)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>formatField (model, name, required, reversed)](#apidoc.element.orm.Utilities.formatField)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>getConditions (model, fields, from)](#apidoc.element.orm.Utilities.getConditions)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>getRealPath (path_str, stack_index)](#apidoc.element.orm.Utilities.getRealPath)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>hasValues (obj, keys)](#apidoc.element.orm.Utilities.hasValues)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>populateConditions (model, fields, source, target, overwrite)](#apidoc.element.orm.Utilities.populateConditions)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>renameDatastoreFieldsToPropertyNames (data, fieldToPropertyMap)](#apidoc.element.orm.Utilities.renameDatastoreFieldsToPropertyNames)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>standardizeOrder (order)](#apidoc.element.orm.Utilities.standardizeOrder)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>transformOrderPropertyNames (order, properties)](#apidoc.element.orm.Utilities.transformOrderPropertyNames)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>transformPropertyNames (dataIn, properties)](#apidoc.element.orm.Utilities.transformPropertyNames)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>values (obj, keys)](#apidoc.element.orm.Utilities.values)
1.  [function <span class="apidocSignatureSpan">orm.Utilities.</span>wrapFieldObject (params)](#apidoc.element.orm.Utilities.wrapFieldObject)

#### [module orm.enforce](#apidoc.module.orm.enforce)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>Enforce (options)](#apidoc.element.orm.enforce.Enforce)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>Validator (validate)](#apidoc.element.orm.enforce.Validator)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>equalToProperty (name, msg)](#apidoc.element.orm.enforce.equalToProperty)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>notEmptyString (message)](#apidoc.element.orm.enforce.notEmptyString)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>required (message)](#apidoc.element.orm.enforce.required)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>sameAs (property, message)](#apidoc.element.orm.enforce.sameAs)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>unique ()](#apidoc.element.orm.enforce.unique)
1.  object <span class="apidocSignatureSpan">orm.enforce.</span>lists
1.  object <span class="apidocSignatureSpan">orm.enforce.</span>patterns
1.  object <span class="apidocSignatureSpan">orm.enforce.</span>ranges
1.  object <span class="apidocSignatureSpan">orm.enforce.</span>security

#### [module orm.enforce.Enforce](#apidoc.module.orm.enforce.Enforce)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>Enforce (options)](#apidoc.element.orm.enforce.Enforce.Enforce)

#### [module orm.enforce.Enforce.prototype](#apidoc.module.orm.enforce.Enforce.prototype)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Enforce.prototype.</span>add (property, validator)](#apidoc.element.orm.enforce.Enforce.prototype.add)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Enforce.prototype.</span>check (data, cb)](#apidoc.element.orm.enforce.Enforce.prototype.check)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Enforce.prototype.</span>clear ()](#apidoc.element.orm.enforce.Enforce.prototype.clear)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Enforce.prototype.</span>context (name, value)](#apidoc.element.orm.enforce.Enforce.prototype.context)

#### [module orm.enforce.Validator](#apidoc.module.orm.enforce.Validator)
1.  [function <span class="apidocSignatureSpan">orm.enforce.</span>Validator (validate)](#apidoc.element.orm.enforce.Validator.Validator)

#### [module orm.enforce.Validator.prototype](#apidoc.module.orm.enforce.Validator.prototype)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>ifDefined ()](#apidoc.element.orm.enforce.Validator.prototype.ifDefined)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>ifNotEmptyString ()](#apidoc.element.orm.enforce.Validator.prototype.ifNotEmptyString)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>ifNotType (type)](#apidoc.element.orm.enforce.Validator.prototype.ifNotType)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>ifType (type)](#apidoc.element.orm.enforce.Validator.prototype.ifType)
1.  [function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>validate (data, next, thisArg, contexts)](#apidoc.element.orm.enforce.Validator.prototype.validate)

#### [module orm.enforce.lists](#apidoc.module.orm.enforce.lists)
1.  [function <span class="apidocSignatureSpan">orm.enforce.lists.</span>inside (list, message)](#apidoc.element.orm.enforce.lists.inside)
1.  [function <span class="apidocSignatureSpan">orm.enforce.lists.</span>outside (list, message)](#apidoc.element.orm.enforce.lists.outside)

#### [module orm.enforce.patterns](#apidoc.module.orm.enforce.patterns)
1.  [function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>email (message)](#apidoc.element.orm.enforce.patterns.email)
1.  [function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>hexString (message)](#apidoc.element.orm.enforce.patterns.hexString)
1.  [function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>ipv4 (message)](#apidoc.element.orm.enforce.patterns.ipv4)
1.  [function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>ipv6 (message)](#apidoc.element.orm.enforce.patterns.ipv6)
1.  [function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>mac (message)](#apidoc.element.orm.enforce.patterns.mac)
1.  [function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>match (pattern, modifiers, message)](#apidoc.element.orm.enforce.patterns.match)
1.  [function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>uuid3 (message)](#apidoc.element.orm.enforce.patterns.uuid3)
1.  [function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>uuid4 (message)](#apidoc.element.orm.enforce.patterns.uuid4)

#### [module orm.enforce.ranges](#apidoc.module.orm.enforce.ranges)
1.  [function <span class="apidocSignatureSpan">orm.enforce.ranges.</span>length (min, max, message)](#apidoc.element.orm.enforce.ranges.length)
1.  [function <span class="apidocSignatureSpan">orm.enforce.ranges.</span>number (min, max, message)](#apidoc.element.orm.enforce.ranges.number)

#### [module orm.enforce.security](#apidoc.module.orm.enforce.security)
1.  [function <span class="apidocSignatureSpan">orm.enforce.security.</span>creditcard (types, message)](#apidoc.element.orm.enforce.security.creditcard)
1.  [function <span class="apidocSignatureSpan">orm.enforce.security.</span>password (checks, message)](#apidoc.element.orm.enforce.security.password)
1.  [function <span class="apidocSignatureSpan">orm.enforce.security.</span>username (options, message)](#apidoc.element.orm.enforce.security.username)

#### [module orm.settings](#apidoc.module.orm.settings)
1.  [function <span class="apidocSignatureSpan">orm.settings.</span>get (key, def)](#apidoc.element.orm.settings.get)
1.  [function <span class="apidocSignatureSpan">orm.settings.</span>set (key, value)](#apidoc.element.orm.settings.set)
1.  [function <span class="apidocSignatureSpan">orm.settings.</span>unset ()](#apidoc.element.orm.settings.unset)

#### [module orm.singleton](#apidoc.module.orm.singleton)
1.  [function <span class="apidocSignatureSpan">orm.singleton.</span>clear (key)](#apidoc.element.orm.singleton.clear)
1.  [function <span class="apidocSignatureSpan">orm.singleton.</span>get (key, opts, createCb, returnCb)](#apidoc.element.orm.singleton.get)

#### [module orm.validators](#apidoc.module.orm.validators)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>equalToProperty (name, msg)](#apidoc.element.orm.validators.equalToProperty)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>insideList (list, message)](#apidoc.element.orm.validators.insideList)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>notEmptyString (message)](#apidoc.element.orm.validators.notEmptyString)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>outsideList (list, message)](#apidoc.element.orm.validators.outsideList)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>password (checks, message)](#apidoc.element.orm.validators.password)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>rangeLength (min, max, message)](#apidoc.element.orm.validators.rangeLength)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>rangeNumber (min, max, message)](#apidoc.element.orm.validators.rangeNumber)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>required (message)](#apidoc.element.orm.validators.required)
1.  [function <span class="apidocSignatureSpan">orm.validators.</span>unique ()](#apidoc.element.orm.validators.unique)
1.  object <span class="apidocSignatureSpan">orm.validators.</span>patterns



# <a name="apidoc.module.orm"></a>[module orm](#apidoc.module.orm)

#### <a name="apidoc.element.orm.Error"></a>[function <span class="apidocSignatureSpan">orm.</span>Error (message, code, extras)](#apidoc.element.orm.Error)
- description and source-code
```javascript
function ORMError(message, code, extras) {
  Error.call(this);
  Error.captureStackTrace(this, this.constructor);

  this.message = message;
  if (code) {
  	this.code = codes[code];
    this.literalCode = code;
    if (!this.code) {
  		throw new Error("Invalid error code: " +  code);
  	}
  }
  if (extras) {
  	for(var k in extras) {
  		this[k] = extras[k];
  	}
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Text"></a>[function <span class="apidocSignatureSpan">orm.</span>Text (data)](#apidoc.element.orm.Text)
- description and source-code
```javascript
Text = function (data) {
		var o = { data: data };

		Object.defineProperty(o, "type", {
			value: function () {
				return type;
			},
			enumerable: false
		});

		return o;
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.addAdapter"></a>[function <span class="apidocSignatureSpan">orm.</span>addAdapter (name, constructor)](#apidoc.element.orm.addAdapter)
- description and source-code
```javascript
function addAdapter(name, constructor) {
  adapters[name] = constructor;
}
```
- example usage
```shell
...

## Adding external database adapters

To add an external database adapter to 'orm', call the 'addAdapter' method, passing in the alias to use for connecting
with this adapter, along with the constructor for the adapter:

'''js
require('orm').addAdapter('cassandra', CassandraAdapter);
'''

See [the documentation for creating adapters](./Adapters.md) for more details.
...
```

#### <a name="apidoc.element.orm.between"></a>[function <span class="apidocSignatureSpan">orm.</span>between (a, b)](#apidoc.element.orm.between)
- description and source-code
```javascript
between = function (a, b) {
	return createSpecialObject({ from: a, to: b }, 'between');
}
```
- example usage
```shell
...
'''js
{ col1: orm.eq(123) } // 'col1' = 123 (default)
{ col1: orm.ne(123) } // 'col1' <> 123
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
{ col1: orm.not_like(12 + "%") } // 'col1' NOT LIKE '12%'
{ col1: orm.not_in([1, 4, 8]) } // 'col1' NOT IN (1, 4, 8)
'''

#### Raw queries
...
```

#### <a name="apidoc.element.orm.connect"></a>[function <span class="apidocSignatureSpan">orm.</span>connect (opts, cb)](#apidoc.element.orm.connect)
- description and source-code
```javascript
connect = function (opts, cb) {
	if (arguments.length === 0 || !opts) {
		return ORM_Error(new ORMError("CONNECTION_URL_EMPTY", 'PARAM_MISMATCH'), cb);
	}
	if (typeof opts == 'string') {
		if (opts.trim().length === 0) {
			return ORM_Error(new ORMError("CONNECTION_URL_EMPTY", 'PARAM_MISMATCH'), cb);
		}
		opts = url.parse(opts, true);
	} else if (typeof opts == 'object') {
		opts = _.cloneDeep(opts);
	}

	opts.query = opts.query || {};

	for(var k in opts.query) {
		opts.query[k] = queryParamCast(opts.query[k]);
		opts[k] = opts.query[k];
	}

	if (!opts.database) {
		// if (!opts.pathname) {
		// 	return cb(new Error("CONNECTION_URL_NO_DATABASE"));
		// }
		opts.database = (opts.pathname ? opts.pathname.substr(1) : "");
	}
	if (!opts.protocol) {
		return ORM_Error(new ORMError("CONNECTION_URL_NO_PROTOCOL", 'PARAM_MISMATCH'), cb);
	}
	// if (!opts.host) {
	// 	opts.host = opts.hostname = "localhost";
	// }
	if (opts.auth) {
		opts.user = opts.auth.split(":")[0];
		opts.password = opts.auth.split(":")[1];
	}
	if (!opts.hasOwnProperty("user")) {
		opts.user = "root";
	}
	if (!opts.hasOwnProperty("password")) {
		opts.password = "";
	}
	if (opts.hasOwnProperty("hostname")) {
		opts.host = opts.hostname;
	}

	var proto  = opts.protocol.replace(/:$/, '');
	var db;
	if (DriverAliases[proto]) {
		proto = DriverAliases[proto];
	}

	try {
		var Driver   = adapters.get(proto);
		var settings = new Settings.Container(exports.settings.get('*'));
		var driver   = new Driver(opts, null, {
			debug    : 'debug' in opts.query ? opts.query.debug : settings.get("connection.debug"),
			pool     : 'pool'  in opts.query ? opts.query.pool  : settings.get("connection.pool"),
			settings : settings
		});

		db = new ORM(proto, driver, settings);

		driver.connect(function (err) {
			if (typeof cb === "function") {
				if (err) {
					return cb(err);
				} else {
					return cb(null, db);
				}
			}

			db.emit("connect", err, !err ? db : null);
		});
	} catch (ex) {
		if (ex.code === "MODULE_NOT_FOUND" || ex.message.indexOf('find module') > -1) {
			return ORM_Error(new ORMError("Connection protocol not supported - have you installed the database driver for " + proto + "?", '
NO_SUPPORT'), cb);
		}
		return ORM_Error(ex, cb);
	}

	return db;
}
```
- example usage
```shell
...
This is a node.js object relational mapping module.

An example:

'''js
var orm = require("orm");

orm.connect("mysql://username:password@host/database", function (err, db) {
  if (err) throw err;

	var Person = db.define("person", {
		name      : String,
		surname   : String,
		age       : Number, // FLOAT
		male      : Boolean,
...
```

#### <a name="apidoc.element.orm.enforce.Enforce"></a>[function <span class="apidocSignatureSpan">orm.</span>enforce.Enforce (options)](#apidoc.element.orm.enforce.Enforce)
- description and source-code
```javascript
function Enforce(options) {
    this.validations = {};
    this.contexts = {};
    this.options = {
        returnAllErrors: options && !!options.returnAllErrors
    };

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.Validator"></a>[function <span class="apidocSignatureSpan">orm.</span>enforce.Validator (validate)](#apidoc.element.orm.enforce.Validator)
- description and source-code
```javascript
function Validator(validate) {
    this.validator = validate;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.eq"></a>[function <span class="apidocSignatureSpan">orm.</span>eq (v)](#apidoc.element.orm.eq)
- description and source-code
```javascript
eq = function (v) {
	return createSpecialObject({ val: v }, 'eq');
}
```
- example usage
```shell
...
{ col1: [ 1, 3, 5 ] } // 'col1' IN (1, 3, 5)
'''

If you need other comparisons, you have to use a special object created by some helper functions. Here are
a few examples to describe it:

'''js
{ col1: orm.eq(123) } // 'col1' = 123 (default)
{ col1: orm.ne(123) } // 'col1' <> 123
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
...
```

#### <a name="apidoc.element.orm.express"></a>[function <span class="apidocSignatureSpan">orm.</span>express ()](#apidoc.element.orm.express)
- description and source-code
```javascript
express = function () {
	return require("./Express").apply(this, arguments);
}
```
- example usage
```shell
...
If you're using Express, you might want to use the simple middleware to integrate more easily.

'''js
var express = require('express');
var orm = require('orm');
var app = express();

app.use(orm.express("mysql://username:password@host/database", {
	define: function (db, models, next) {
		models.person = db.define("person", { ... });
		next();
	}
}));
app.listen(80);
...
```

#### <a name="apidoc.element.orm.gt"></a>[function <span class="apidocSignatureSpan">orm.</span>gt (v)](#apidoc.element.orm.gt)
- description and source-code
```javascript
gt = function (v) {
	return createSpecialObject({ val: v }, 'gt');
}
```
- example usage
```shell
...

'''js
var Person = db.define('person', {
    name    : String,
    height  : { type: 'integer' }
});
Person.tallerThan = function(height, callback) {
    this.find({ height: orm.gt(height) }, callback);
};

Person.tallerThan( 192, function(err, tallPeople) { ... } );
'''


## Loading Models
...
```

#### <a name="apidoc.element.orm.gte"></a>[function <span class="apidocSignatureSpan">orm.</span>gte (v)](#apidoc.element.orm.gte)
- description and source-code
```javascript
gte = function (v) {
	return createSpecialObject({ val: v }, 'gte');
}
```
- example usage
```shell
...
If you need other comparisons, you have to use a special object created by some helper functions. Here are
a few examples to describe it:

'''js
{ col1: orm.eq(123) } // 'col1' = 123 (default)
{ col1: orm.ne(123) } // 'col1' <> 123
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
{ col1: orm.not_like(12 + "%") } // 'col1' NOT LIKE '12%'
{ col1: orm.not_in([1, 4, 8]) } // 'col1' NOT IN (1, 4, 8)
...
```

#### <a name="apidoc.element.orm.like"></a>[function <span class="apidocSignatureSpan">orm.</span>like (expr)](#apidoc.element.orm.like)
- description and source-code
```javascript
like = function (expr) {
	return createSpecialObject({ expr: expr }, 'like');
}
```
- example usage
```shell
...
{ col1: orm.ne(123) } // 'col1' <> 123
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
{ col1: orm.not_like(12 + "%") } // 'col1' NOT LIKE '12%'
{ col1: orm.not_in([1, 4, 8]) } // 'col1' NOT IN (1, 4, 8)
'''

#### Raw queries

'''js
...
```

#### <a name="apidoc.element.orm.lt"></a>[function <span class="apidocSignatureSpan">orm.</span>lt (v)](#apidoc.element.orm.lt)
- description and source-code
```javascript
lt = function (v) {
	return createSpecialObject({ val: v }, 'lt');
}
```
- example usage
```shell
...
a few examples to describe it:

'''js
{ col1: orm.eq(123) } // 'col1' = 123 (default)
{ col1: orm.ne(123) } // 'col1' <> 123
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
{ col1: orm.not_like(12 + "%") } // 'col1' NOT LIKE '12%'
{ col1: orm.not_in([1, 4, 8]) } // 'col1' NOT IN (1, 4, 8)
'''
...
```

#### <a name="apidoc.element.orm.lte"></a>[function <span class="apidocSignatureSpan">orm.</span>lte (v)](#apidoc.element.orm.lte)
- description and source-code
```javascript
lte = function (v) {
	return createSpecialObject({ val: v }, 'lte');
}
```
- example usage
```shell
...

'''js
{ col1: orm.eq(123) } // 'col1' = 123 (default)
{ col1: orm.ne(123) } // 'col1' <> 123
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
{ col1: orm.not_like(12 + "%") } // 'col1' NOT LIKE '12%'
{ col1: orm.not_in([1, 4, 8]) } // 'col1' NOT IN (1, 4, 8)
'''
...
```

#### <a name="apidoc.element.orm.ne"></a>[function <span class="apidocSignatureSpan">orm.</span>ne (v)](#apidoc.element.orm.ne)
- description and source-code
```javascript
ne = function (v) {
	return createSpecialObject({ val: v }, 'ne');
}
```
- example usage
```shell
...
'''

If you need other comparisons, you have to use a special object created by some helper functions. Here are
a few examples to describe it:

'''js
{ col1: orm.eq(123) } // 'col1' = 123 (default)
{ col1: orm.ne(123) } // 'col1' <> 123
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
...
```

#### <a name="apidoc.element.orm.not_between"></a>[function <span class="apidocSignatureSpan">orm.</span>not_between (a, b)](#apidoc.element.orm.not_between)
- description and source-code
```javascript
not_between = function (a, b) {
	return createSpecialObject({ from: a, to: b }, 'not_between');
}
```
- example usage
```shell
...
{ col1: orm.eq(123) } // 'col1' = 123 (default)
{ col1: orm.ne(123) } // 'col1' <> 123
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
{ col1: orm.not_like(12 + "%") } // 'col1' NOT LIKE '12%'
{ col1: orm.not_in([1, 4, 8]) } // 'col1' NOT IN (1, 4, 8)
'''

#### Raw queries
...
```

#### <a name="apidoc.element.orm.not_in"></a>[function <span class="apidocSignatureSpan">orm.</span>not_in (v)](#apidoc.element.orm.not_in)
- description and source-code
```javascript
not_in = function (v) {
	return createSpecialObject({ val: v }, 'not_in');
}
```
- example usage
```shell
...
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
{ col1: orm.not_like(12 + "%") } // 'col1' NOT LIKE '12%'
{ col1: orm.not_in([1, 4, 8]) } // 'col1' NOT IN (1, 4, 8)
'''

#### Raw queries

'''js
db.driver.execQuery("SELECT id, email FROM user", function (err, data) { ... })
...
```

#### <a name="apidoc.element.orm.not_like"></a>[function <span class="apidocSignatureSpan">orm.</span>not_like (expr)](#apidoc.element.orm.not_like)
- description and source-code
```javascript
not_like = function (expr) {
	return createSpecialObject({ expr: expr }, 'not_like');
}
```
- example usage
```shell
...
{ col1: orm.gt(123) } // 'col1' > 123
{ col1: orm.gte(123) } // 'col1' >= 123
{ col1: orm.lt(123) } // 'col1' < 123
{ col1: orm.lte(123) } // 'col1' <= 123
{ col1: orm.between(123, 456) } // 'col1' BETWEEN 123 AND 456
{ col1: orm.not_between(123, 456) } // 'col1' NOT BETWEEN 123 AND 456
{ col1: orm.like(12 + "%") } // 'col1' LIKE '12%'
{ col1: orm.not_like(12 + "%") } // 'col1' NOT LIKE '12%'
{ col1: orm.not_in([1, 4, 8]) } // 'col1' NOT IN (1, 4, 8)
'''

#### Raw queries

'''js
db.driver.execQuery("SELECT id, email FROM user", function (err, data) { ... })
...
```

#### <a name="apidoc.element.orm.use"></a>[function <span class="apidocSignatureSpan">orm.</span>use (connection, proto, opts, cb)](#apidoc.element.orm.use)
- description and source-code
```javascript
use = function (connection, proto, opts, cb) {
	if (DriverAliases[proto]) {
		proto = DriverAliases[proto];
	}
	if (typeof opts === "function") {
		cb = opts;
		opts = {};
	}

	try {
		var Driver   = adapters.get(proto);
		var settings = new Settings.Container(exports.settings.get('*'));
		var driver   = new Driver(null, connection, {
			debug    : (opts.query && opts.query.debug === 'true'),
			settings : settings
		});

		return cb(null, new ORM(proto, driver, settings));
	} catch (ex) {
		return cb(ex);
	}
}
```
- example usage
```shell
...
If you're using Express, you might want to use the simple middleware to integrate more easily.

'''js
var express = require('express');
var orm = require('orm');
var app = express();

app.use(orm.express("mysql://username:password@host/database", {
	define: function (db, models, next) {
		models.person = db.define("person", { ... });
		next();
	}
}));
app.listen(80);
...
```



# <a name="apidoc.module.orm.Adapters"></a>[module orm.Adapters](#apidoc.module.orm.Adapters)

#### <a name="apidoc.element.orm.Adapters.add"></a>[function <span class="apidocSignatureSpan">orm.Adapters.</span>add (name, constructor)](#apidoc.element.orm.Adapters.add)
- description and source-code
```javascript
function addAdapter(name, constructor) {
  adapters[name] = constructor;
}
```
- example usage
```shell
...
						}
					}
				}
				if (!alwaysValidate && !required && instance[k] == null) {
					continue; // avoid validating if property is not required and is "empty"
				}
				for (i = 0; i < opts.validations[k].length; i++) {
					checks.add(k, opts.validations[k][i]);
				}
			}

			checks.context("instance", instance);
			checks.context("model", Model);
			checks.context("driver", opts.driver);
...
```

#### <a name="apidoc.element.orm.Adapters.get"></a>[function <span class="apidocSignatureSpan">orm.Adapters.</span>get (name)](#apidoc.element.orm.Adapters.get)
- description and source-code
```javascript
function getAdapter(name) {
  if (name in aliases) {
    return getAdapter(aliases[name]);
  } else if (!(name in adapters)) {
    adapters[name] = require("./Drivers/DML/" + name).Driver;
  }

  return adapters[name];
}
```
- example usage
```shell
...
	define: function (db, models, next) {
		models.person = db.define("person", { ... });
		next();
	}
}));
app.listen(80);

app.get("/", function (req, res) {
	// req.models is a reference to models used above in define()
	req.models.person.find(...);
});
'''

You can call 'orm.express' more than once to have multiple database connections. Models defined across connections
will be joined together in 'req.models'. **Don't forget to use it before 'app.use(app.router)', preferably right after your
...
```



# <a name="apidoc.module.orm.Debug"></a>[module orm.Debug](#apidoc.module.orm.Debug)

#### <a name="apidoc.element.orm.Debug.sql"></a>[function <span class="apidocSignatureSpan">orm.Debug.</span>sql (driver, sql)](#apidoc.element.orm.Debug.sql)
- description and source-code
```javascript
sql = function (driver, sql) {
	var fmt;

	if (tty.isatty(process.stdout)) {
		fmt = "\033[32;1m(orm/%s) \033[34m%s\033[0m\n";
		sql = sql.replace(/'(.+?)'/g, function (m) { return "\033[31m" + m + "\033[34m"; });
	} else {
		fmt = "[SQL/%s] %s\n";
	}

	process.stdout.write(util.format(fmt, driver, sql));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.Error"></a>[module orm.Error](#apidoc.module.orm.Error)

#### <a name="apidoc.element.orm.Error.Error"></a>[function <span class="apidocSignatureSpan">orm.</span>Error (message, code, extras)](#apidoc.element.orm.Error.Error)
- description and source-code
```javascript
function ORMError(message, code, extras) {
  Error.call(this);
  Error.captureStackTrace(this, this.constructor);

  this.message = message;
  if (code) {
  	this.code = codes[code];
    this.literalCode = code;
    if (!this.code) {
  		throw new Error("Invalid error code: " +  code);
  	}
  }
  if (extras) {
  	for(var k in extras) {
  		this[k] = extras[k];
  	}
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.Error.prototype"></a>[module orm.Error.prototype](#apidoc.module.orm.Error.prototype)

#### <a name="apidoc.element.orm.Error.prototype.constructor"></a>[function <span class="apidocSignatureSpan">orm.Error.prototype.</span>constructor (message, code, extras)](#apidoc.element.orm.Error.prototype.constructor)
- description and source-code
```javascript
function ORMError(message, code, extras) {
  Error.call(this);
  Error.captureStackTrace(this, this.constructor);

  this.message = message;
  if (code) {
  	this.code = codes[code];
    this.literalCode = code;
    if (!this.code) {
  		throw new Error("Invalid error code: " +  code);
  	}
  }
  if (extras) {
  	for(var k in extras) {
  		this[k] = extras[k];
  	}
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Error.prototype.toString"></a>[function <span class="apidocSignatureSpan">orm.Error.prototype.</span>toString ()](#apidoc.element.orm.Error.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return '[ORMError ' + this.literalCode + ': ' + this.message + ']';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.Hook"></a>[module orm.Hook](#apidoc.module.orm.Hook)

#### <a name="apidoc.element.orm.Hook.trigger"></a>[function <span class="apidocSignatureSpan">orm.Hook.</span>trigger ()](#apidoc.element.orm.Hook.trigger)
- description and source-code
```javascript
trigger = function () {
	var args = Array.prototype.slice.apply(arguments);
	var self = args.shift();
	var cb   = args.shift();

	if (typeof cb === "function") {
		cb.apply(self, args);
	}
}
```
- example usage
```shell
...
		});
	};
	var saveError = function (cb, err) {
		instance_saving = false;

		emitEvent("save", err, instance);

		Hook.trigger(instance, opts.hooks.afterSave, false);

		if (typeof cb === "function") {
			cb(err, instance);
		}
	};
	var saveInstance = function (saveOptions, cb) {
		// what this condition means:
...
```

#### <a name="apidoc.element.orm.Hook.wait"></a>[function <span class="apidocSignatureSpan">orm.Hook.</span>wait ()](#apidoc.element.orm.Hook.wait)
- description and source-code
```javascript
wait = function () {
	var args = Array.prototype.slice.apply(arguments);
	var self = args.shift();
	var cb   = args.shift();
	var next = args.shift();

	args.push(next);

	if (typeof cb === "function") {
		cb.apply(self, args);

		if (cb.length < args.length) {
			return next();
		}
	} else {
		return next();
	}
}
```
- example usage
```shell
...
		} else {
			return !!saveOptions.saveAssociations;
		}
	};
	var handleValidations = function (cb) {
		var pending = [], errors = [], required, alwaysValidate;

		Hook.wait(instance, opts.hooks.beforeValidation, function (err) {
		    var k, i;
			if (err) {
				return saveError(cb, err);
			}

			var checks = new enforce.Enforce({
				returnAllErrors : Model.settings.get("instance.returnAllErrors")
...
```



# <a name="apidoc.module.orm.Instance"></a>[module orm.Instance](#apidoc.module.orm.Instance)

#### <a name="apidoc.element.orm.Instance.Instance"></a>[function <span class="apidocSignatureSpan">orm.</span>Instance (Model, opts)](#apidoc.element.orm.Instance.Instance)
- description and source-code
```javascript
function Instance(Model, opts) {
	opts = opts || {};
	opts.data = opts.data || {};
	opts.extra = opts.extra || {};
	opts.keys = opts.keys || "id";
	opts.changes = (opts.is_new ? Object.keys(opts.data) : []);
	opts.extrachanges = [];
	opts.associations = {};
	opts.originalKeyValues = {};

	var instance_saving = false;
	var events = {};
	var instance = {};
	var emitEvent = function () {
		var args = Array.prototype.slice.apply(arguments);
		var event = args.shift();

		if (!events.hasOwnProperty(event)) return;

		events[event].map(function (cb) {
			cb.apply(instance, args);
		});
	};
	var rememberKeys = function () {
		var i, prop;

		for(i = 0; i < opts.keyProperties.length; i++) {
			prop = opts.keyProperties[i];
			opts.originalKeyValues[prop.name] = opts.data[prop.name];
		}
	};
	var shouldSaveAssocs = function (saveOptions) {
		if (Model.settings.get("instance.saveAssociationsByDefault")) {
			return saveOptions.saveAssociations !== false;
		} else {
			return !!saveOptions.saveAssociations;
		}
	};
	var handleValidations = function (cb) {
		var pending = [], errors = [], required, alwaysValidate;

		Hook.wait(instance, opts.hooks.beforeValidation, function (err) {
		    var k, i;
			if (err) {
				return saveError(cb, err);
			}

			var checks = new enforce.Enforce({
				returnAllErrors : Model.settings.get("instance.returnAllErrors")
			});

			for (k in opts.validations) {
				required = false;

				if (Model.allProperties[k]) {
					required = Model.allProperties[k].required;
					alwaysValidate = Model.allProperties[k].alwaysValidate;
				} else {
					for (i = 0; i < opts.one_associations.length; i++) {
						if (opts.one_associations[i].field === k) {
							required = opts.one_associations[i].required;
							break;
						}
					}
				}
				if (!alwaysValidate && !required && instance[k] == null) {
					continue; // avoid validating if property is not required and is "empty"
				}
				for (i = 0; i < opts.validations[k].length; i++) {
					checks.add(k, opts.validations[k][i]);
				}
			}

			checks.context("instance", instance);
			checks.context("model", Model);
			checks.context("driver", opts.driver);

			return checks.check(instance, cb);
		});
	};
	var saveError = function (cb, err) {
		instance_saving = false;

		emitEvent("save", err, instance);

		Hook.trigger(instance, opts.hooks.afterSave, false);

		if (typeof cb === "function") {
			cb(err, instance);
		}
	};
	var saveInstance = function (saveOptions, cb) {
		// what this condition means:
		// - If the instance is in state mode
		// - AND it's not an association that is asking it to save
		//   -> return has already saved
		if (instance_saving && saveOptions.saveAssociations !== false) {
			return cb(null, instance);
		}
		instance_saving = true;

		handleValidations(function (err) {
			if (err) {
				return saveError(cb, err);
			}

			if (opts.is_new) {
				waitHooks([ "beforeCreate", "beforeSave" ], function (err) {
					if (err) {
						return saveError(cb, err);
					}

					return saveNew(saveOptions, getInstanceData(), cb);
				});
			} else {
				waitHooks([ "beforeSave" ], function (err) {
					if (err) {
						return saveError(cb, err);
					}

					return savePersisted(saveOptions, getInstanceData(), cb);
				});
			}
		});
	};
	var runAfterSaveActions = function (cb, create, err) {
		instance_saving = false;

		emitEvent("save", err, instance);

		if (create) {
			Hook.trigger(instance, opts.hooks.afterCreate, !err);
		}
		Hook.trigger(instance, opts.hooks.afterSave, !err);

		cb();
	};
	var getInstanceData = function () {
		var data = {}, prop;
		for (var k in opts.data) {
			if (!opts.data.hasOwnProperty(k)) continue;
			prop = Model.allProperties[k];

			if (prop) {
				if (opts.data[k] == null &&  (prop.type == 'serial' || typeof prop.defaultValue == 'function')) {
					continue;
				}

				if (opts.driver.propertyToValue) {
					data[k] = opts.driver.propertyToValue(opts.data[k], prop);
				} else {
					data[k] = opts.data[k];
				}
			} else {
				data[k] = opts.data[k];
			}
		}

		return data;
	};
	var waitHooks = function ( ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.LazyLoad"></a>[module orm.LazyLoad](#apidoc.module.orm.LazyLoad)

#### <a name="apidoc.element.orm.LazyLoad.extend"></a>[function <span class="apidocSignatureSpan">orm.LazyLoad.</span>extend (Instance, Model, properties)](#apidoc.element.orm.LazyLoad.extend)
- description and source-code
```javascript
extend = function (Instance, Model, properties) {
	for (var k in properties) {
		if (properties[k].lazyload === true) {
			addLazyLoadProperty(properties[k].lazyname || k, Instance, Model, k);
		}
	}
}
```
- example usage
```shell
...
			opts.conditions = opts.conditions || {};

			if (typeof _.last(args) === "function") {
			    cb = args.pop();
			}

			if (typeof args[0] === "object") {
				_.extend(opts.conditions, args[0]);
			} else if (typeof args[0] === "string") {
				opts.conditions.__sql = opts.conditions.__sql || [];
				opts.conditions.__sql.push(args);
			}

			if (cb) {
				chainRun(cb);
...
```



# <a name="apidoc.module.orm.Model"></a>[module orm.Model](#apidoc.module.orm.Model)

#### <a name="apidoc.element.orm.Model.Model"></a>[function <span class="apidocSignatureSpan">orm.</span>Model (opts)](#apidoc.element.orm.Model.Model)
- description and source-code
```javascript
function Model(opts) {
	opts = _.defaults(opts || {}, {
		keys: []
	});
	opts.keys = Array.isArray(opts.keys) ? opts.keys : [opts.keys];

	var one_associations       = [];
	var many_associations      = [];
	var extend_associations    = [];
	var association_properties = [];
	var model_fields           = [];
	var fieldToPropertyMap     = {};
	var allProperties          = {};
	var keyProperties          = [];

	var createHookHelper = function (hook) {
		return function (cb) {
			if (typeof cb !== "function") {
				delete opts.hooks[hook];
			} else {
				opts.hooks[hook] = cb;
			}
			return this;
		};
	};
	var createInstance = function (data, inst_opts, cb) {
		if (!inst_opts) {
			inst_opts = {};
		}

		var found_assoc = false, i, k;

		for (k in data) {
			if (k === "extra_field") continue;
			if (opts.properties.hasOwnProperty(k)) continue;
			if (inst_opts.extra && inst_opts.extra.hasOwnProperty(k)) continue;
			if (opts.keys.indexOf(k) >= 0) continue;
			if (association_properties.indexOf(k) >= 0) continue;

			for (i = 0; i < one_associations.length; i++) {
				if (one_associations[i].name === k) {
					found_assoc = true;
					break;
				}
			}
			if (!found_assoc) {
				for (i = 0; i < many_associations.length; i++) {
					if (many_associations[i].name === k) {
						found_assoc = true;
						break;
					}
				}
			}
			if (!found_assoc) {
				delete data[k];
			}
		}

		var assoc_opts = {
			autoFetch      : inst_opts.autoFetch || false,
			autoFetchLimit : inst_opts.autoFetchLimit,
			cascadeRemove  : inst_opts.cascadeRemove
		};

		var setupAssociations = function (instance) {
			OneAssociation.extend(model, instance, opts.driver, one_associations, assoc_opts);
			ManyAssociation.extend(model, instance, opts.driver, many_associations, assoc_opts, createInstance);
			ExtendAssociation.extend(model, instance, opts.driver, extend_associations, assoc_opts);
		};

		var pending  = 2, create_err = null;
		var instance = new Instance(model, {
			uid                    : inst_opts.uid, // singleton unique id
			keys                   : opts.keys,
			is_new                 : inst_opts.is_new || false,
			isShell                : inst_opts.isShell || false,
			data                   : data,
			autoSave               : inst_opts.autoSave || false,
			extra                  : inst_opts.extra,
			extra_info             : inst_opts.extra_info,
			driver                 : opts.driver,
			table                  : opts.table,
			hooks                  : opts.hooks,
			methods                : opts.methods,
			validations            : opts.validations,
			one_associations       : one_associations,
			many_associations      : many_associations,
			extend_associations    : extend_associations,
			association_properties : association_properties,
			setupAssociations      : setupAssociations,
			fieldToPropertyMap     : fieldToPropertyMap,
			keyProperties          : keyProperties
		});
		instance.on("ready", function (err) {
			if (--pending > 0) {
				create_err = err;
				return;
			}
			if (typeof cb === "function") {
				return cb(err || create_err, instance);
			}
		});
		if (model_fields !== null) {
			LazyLoad.extend(instance, model, opts.properties);
		}

		OneAssociation.autoFetch(instance, one_associations, assoc_opts, function () {
			ManyAssociation.autoFetch(instance, many_associations, assoc_opts, function () {
				ExtendAssociation.autoFetch(instance, extend_associations, assoc_opts, function () {
					Hook.wait(instance, opts.hooks.afterAutoFetch, function (err) {
						if (--pending > 0) {
							create_err = err;
							return;
						}
						if (typeof cb === "function") {
							return cb(err || create_err, instance);
						}
					});
				});
			});
		});
		return instance;
	};

	var model = function () {
	    var instance, i;

	    var data = arguments.length > 1 ? arguments : arguments[0];

	    if (Array.isArray(opts.keys) && Array.isArray(data)) {
	        if (data.length == opts.keys.length) {
	            var data2 = {};
	            for (i = 0; i < opts.keys.length; i++) {
	                data2[opts.keys[i ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.Promise"></a>[module orm.Promise](#apidoc.module.orm.Promise)

#### <a name="apidoc.element.orm.Promise.Promise"></a>[function <span class="apidocSignatureSpan">orm.</span>Promise (opts)](#apidoc.element.orm.Promise.Promise)
- description and source-code
```javascript
function Promise(opts) {
	opts = opts || {};

	var success_cb = opts.success || null;
	var fail_cb    = opts.fail    || null;

	return {
		handle: function (promise) {
			promise(function (err) {
				if (err) {
					if (fail_cb) fail_cb(err);
				} else {
					var args = Array.prototype.slice.call(arguments, 1);

					if (success_cb) success_cb.apply(null, args);
				}
			});
		},
		success: function (cb) {
			success_cb = cb;
			return this;
		},
		fail: function (cb) {
			fail_cb = cb;
			return this;
		}
	};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.Property"></a>[module orm.Property](#apidoc.module.orm.Property)

#### <a name="apidoc.element.orm.Property.normalize"></a>[function <span class="apidocSignatureSpan">orm.Property.</span>normalize (opts)](#apidoc.element.orm.Property.normalize)
- description and source-code
```javascript
normalize = function (opts) {
	if (typeof opts.prop === "function") {
		switch (opts.prop.name) {
			case "String":
				opts.prop = { type: "text" };
				break;
			case "Number":
				opts.prop = { type: "number" };
				break;
			case "Boolean":
				opts.prop = { type: "boolean" };
				break;
			case "Date":
				opts.prop = { type: "date" };
				break;
			case "Object":
				opts.prop = { type: "object" };
				break;
			case "Buffer":
				opts.prop = { type: "binary" };
				break;
		}
	} else if (typeof opts.prop === "string") {
		var tmp = opts.prop;
		opts.prop = {};
		opts.prop.type = tmp;
	} else if (Array.isArray(opts.prop)) {
		opts.prop = { type: "enum", values: opts.prop };
	} else {
		opts.prop = _.cloneDeep(opts.prop);
	}

	if (KNOWN_TYPES.indexOf(opts.prop.type) === -1 && !(opts.prop.type in opts.customTypes)) {
		throw new ORMError("Unknown property type: " + opts.prop.type, 'NO_SUPPORT');
	}

	if (!opts.prop.hasOwnProperty("required") && opts.settings.get("properties.required")) {
		opts.prop.required = true;
	}

	// Defaults to true. Setting to false hides properties from JSON.stringify(modelInstance).
	if (!opts.prop.hasOwnProperty("enumerable") || opts.prop.enumerable === true) {
		opts.prop.enumerable = true;
	}

	// Defaults to true. Rational means floating point here.
	if (opts.prop.type == "number" && opts.prop.rational === undefined) {
		opts.prop.rational = true;
	}

	if (!('mapsTo' in opts.prop)) {
		opts.prop.mapsTo = opts.name
	}

	if (opts.prop.type == "number" && opts.prop.rational === false) {
		opts.prop.type = "integer";
		delete opts.prop.rational;
	}

	opts.prop.name = opts.name;

	return opts.prop;
}
```
- example usage
```shell
...
		}
	};

	var currFields = {};

	model.addProperty = function (propIn, options) {
		var cType;
		var prop = Property.normalize({
			prop: propIn, name: (options && options.name || propIn.name),
			customTypes: opts.db.customTypes, settings: opts.settings
		});

		// Maintains backwards compatibility
		if (opts.keys.indexOf(k) != -1) {
			prop.key = true;
...
```



# <a name="apidoc.module.orm.Settings"></a>[module orm.Settings](#apidoc.module.orm.Settings)

#### <a name="apidoc.element.orm.Settings.Container"></a>[function <span class="apidocSignatureSpan">orm.Settings.</span>Container (settings)](#apidoc.element.orm.Settings.Container)
- description and source-code
```javascript
function Settings(settings) {
	this.settings = settings;

	return {
		set: function (key, value) {
			set(key, value, settings);

			return this;
		},
		get: function (key, def) {
			var v = get(key, def, settings)

			if (v instanceof Function) {
				return v;
			} else {
				return _.cloneDeep(v);
			}
		},
		unset: function () {
			for (var i = 0; i < arguments.length; i++) {
				if (typeof arguments[i] === "string") {
					unset(arguments[i], settings);
				}
			}

			return this;
		}
	};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Settings.defaults"></a>[function <span class="apidocSignatureSpan">orm.Settings.</span>defaults ()](#apidoc.element.orm.Settings.defaults)
- description and source-code
```javascript
defaults = function () {
	return default_settings;
}
```
- example usage
```shell
...
	"afterLoad",
	"afterAutoFetch"
];

exports.Model = Model;

function Model(opts) {
	opts = _.defaults(opts || {}, {
		keys: []
	});
	opts.keys = Array.isArray(opts.keys) ? opts.keys : [opts.keys];

	var one_associations       = [];
	var many_associations      = [];
	var extend_associations    = [];
...
```



# <a name="apidoc.module.orm.Utilities"></a>[module orm.Utilities](#apidoc.module.orm.Utilities)

#### <a name="apidoc.element.orm.Utilities.checkConditions"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>checkConditions (conditions, one_associations)](#apidoc.element.orm.Utilities.checkConditions)
- description and source-code
```javascript
checkConditions = function (conditions, one_associations) {
	var k, i, j;

	// A)
	var associations = {};
	for (i = 0; i < one_associations.length; i++) {
		associations[one_associations[i].name] = one_associations[i];
	}

	for (k in conditions) {
		// B)
		if (!associations.hasOwnProperty(k)) continue;

		// C)
		var values = conditions[k];
		if (!Array.isArray(values)) values = [values];

		// D)
		delete conditions[k];

		// E)
		var association_fields = Object.keys(associations[k].field);
		var model = associations[k].model;

		// F)
		for (i = 0; i < values.length; i++) {
			if (values[i].isInstance && values[i].model().uid === model.uid) {
				if (association_fields.length === 1) {
					if (typeof conditions[association_fields[0]] === 'undefined') {
						conditions[association_fields[0]] = values[i][model.id[0]];
					} else if(Array.isArray(conditions[association_fields[0]])) {
						conditions[association_fields[0]].push(values[i][model.id[0]]);
					} else {
						conditions[association_fields[0]] = [conditions[association_fields[0]], values[i][model.id[0]]];
					}
				} else {
					var _conds = {};
					for (j = 0; j < association_fields.length; i++) {
						_conds[association_fields[j]] = values[i][model.id[j]];
					}

					conditions.or = conditions.or || [];
					conditions.or.push(_conds);
				}
			}
		}
	}

	return conditions;
}
```
- example usage
```shell
...
			options.cascadeRemove = opts.cascadeRemove;
		}

		if (order) {
			order = Utilities.standardizeOrder(order);
		}
		if (conditions) {
			conditions = Utilities.checkConditions(conditions, one_associations);
		}

		var chain = new ChainFind(model, {
			only         : options.only || model_fields,
			keys         : opts.keys,
			table        : opts.table,
			driver       : opts.driver,
...
```

#### <a name="apidoc.element.orm.Utilities.convertPropToJoinKeyProp"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>convertPropToJoinKeyProp (props, opts)](#apidoc.element.orm.Utilities.convertPropToJoinKeyProp)
- description and source-code
```javascript
convertPropToJoinKeyProp = function (props, opts) {
	var prop;

	for (var k in props) {
		prop = props[k];

		prop.required = opts.required;

		if (prop.type == 'serial') {
			prop.type = 'integer';
		}
		if (opts.makeKey) {
			prop.key = true;
		} else {
			delete prop.key;
		}
	}

	return props;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Utilities.formatField"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>formatField (model, name, required, reversed)](#apidoc.element.orm.Utilities.formatField)
- description and source-code
```javascript
formatField = function (model, name, required, reversed) {
	var fields = {}, field_opts, field_name;
	var keys = model.id;
	var assoc_key = model.settings.get("properties.association_key");

	for (var i = 0; i < keys.length; i++) {
		if (reversed) {
			field_name = keys[i];
		} else if (typeof assoc_key === "function") {
			field_name = assoc_key(name.toLowerCase(), keys[i]);
		} else {
			field_name = assoc_key.replace("{name}", name.toLowerCase())
			                      .replace("{field}", keys[i]);
		}

		if (model.properties.hasOwnProperty(keys[i])) {
			var p = model.properties[keys[i]];

			field_opts = {
				type     : p.type || "integer",
				size     : p.size || 4,
				unsigned : p.unsigned || true,
				time     : p.time || false,
				big      : p.big || false,
				values   : p.values || null,
				required : required,
				name     : field_name,
				mapsTo   : field_name
			};
		} else {
			field_opts = {
				type     : "integer",
				unsigned : true,
				size     : 4,
				required : required,
				name     : field_name,
				mapsTo   : field_name
			};
		}

		fields[field_name] = field_opts;
	}

	return fields;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Utilities.getConditions"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>getConditions (model, fields, from)](#apidoc.element.orm.Utilities.getConditions)
- description and source-code
```javascript
getConditions = function (model, fields, from) {
	var conditions = {};

	exports.populateConditions(model, fields, from, conditions);

	return conditions;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Utilities.getRealPath"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>getRealPath (path_str, stack_index)](#apidoc.element.orm.Utilities.getRealPath)
- description and source-code
```javascript
getRealPath = function (path_str, stack_index) {
	var path = require("path"); // for now, load here (only when needed)
	var cwd = process.cwd();
	var err = new Error();
	var tmp = err.stack.split(/\r?\n/)[typeof stack_index !== "undefined" ? stack_index : 3], m;

	if ((m = tmp.match(/^\s*at\s+(.+):\d+:\d+$/)) !== null) {
		cwd = path.dirname(m[1]);
	} else if ((m = tmp.match(/^\s*at\s+module\.exports\s+\((.+?)\)/)) !== null) {
		cwd = path.dirname(m[1]);
	} else if ((m = tmp.match(/^\s*at\s+.+\s+\((.+):\d+:\d+\)$/)) !== null) {
		cwd = path.dirname(m[1]);
	}
	var pathIsAbsolute = path.isAbsolute || require('path-is-absolute');
	if (!pathIsAbsolute(path_str)) {
		path_str = path.join(cwd, path_str);
	}
	if (path_str.substr(-1) === path.sep) {
		path_str += "index";
	}

	return path_str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Utilities.hasValues"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>hasValues (obj, keys)](#apidoc.element.orm.Utilities.hasValues)
- description and source-code
```javascript
hasValues = function (obj, keys) {
	for (var i = 0; i < keys.length; i++) {
		if (!obj[keys[i]] && obj[keys[i]] !== 0) return false;  // 0 is also a good value...
	}
	return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Utilities.populateConditions"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>populateConditions (model, fields, source, target, overwrite)](#apidoc.element.orm.Utilities.populateConditions)
- description and source-code
```javascript
populateConditions = function (model, fields, source, target, overwrite) {
	for (var i = 0; i < model.id.length; i++) {
		if (typeof target[fields[i]] === 'undefined' || overwrite !== false) {
			target[fields[i]] = source[model.id[i]];
		} else if (Array.isArray(target[fields[i]])) {
			target[fields[i]].push(source[model.id[i]]);
		} else {
			target[fields[i]] = [target[fields[i]], source[model.id[i]]];
		}
	}
}
```
- example usage
```shell
...
		}
	}
};

exports.getConditions = function (model, fields, from) {
	var conditions = {};

	exports.populateConditions(model, fields, from, conditions);

	return conditions;
};

exports.wrapFieldObject = function (params) {
	if (!params.field) {
		var assoc_key = params.model.settings.get("properties.association_key");
...
```

#### <a name="apidoc.element.orm.Utilities.renameDatastoreFieldsToPropertyNames"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>renameDatastoreFieldsToPropertyNames (data, fieldToPropertyMap)](#apidoc.element.orm.Utilities.renameDatastoreFieldsToPropertyNames)
- description and source-code
```javascript
renameDatastoreFieldsToPropertyNames = function (data, fieldToPropertyMap) {
	var k, prop;

	for (k in data) {
		prop = fieldToPropertyMap[k];
		if (prop && prop.name != k) {
			data[prop.name] = data[k];
			delete data[k];
		}
	}
	return data;
}
```
- example usage
```shell
...
			if (err) {
				return cb(new ORMError(err.message, 'QUERY_ERROR', { originalCode: err.code }));
			}
			if (data.length === 0) {
				return cb(new ORMError("Not found", 'NOT_FOUND', { model: opts.table }));
			}

			Utilities.renameDatastoreFieldsToPropertyNames(data[0], fieldToPropertyMap);

			var uid = opts.driver.uid + "/" + opts.table + "/" + ids.join("/");

			Singleton.get(uid, {
				identityCache : (options.hasOwnProperty("identityCache") ? options.identityCache : opts.identityCache),
				saveCheck     : opts.settings.get("instance.identityCacheSaveCheck")
			}, function (cb) {
...
```

#### <a name="apidoc.element.orm.Utilities.standardizeOrder"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>standardizeOrder (order)](#apidoc.element.orm.Utilities.standardizeOrder)
- description and source-code
```javascript
standardizeOrder = function (order) {
	if (typeof order === "string") {
		if (order[0] === "-") {
			return [ [ order.substr(1), "Z" ] ];
		}
		return [ [ order, "A" ] ];
	}

	var new_order = [], minus;

	for (var i = 0; i < order.length; i++) {
		minus = (order[i][0] === "-");

		if (i < order.length - 1 && [ "A", "Z" ].indexOf(order[i + 1].toUpperCase()) >= 0) {
			new_order.push([
				(minus ? order[i].substr(1) : order[i]),
				order[i + 1]
			]);
			i += 1;
		} else if (minus) {
			new_order.push([ order[i].substr(1), "Z" ]);
		} else {
			new_order.push([ order[i], "A" ]);
		}
	}

	return new_order;
}
```
- example usage
```shell
...
				opts.limit = [ offset, limit ];
			} else {
				opts.limit = [ 0, offset ]; // offset = limit
			}
			return this;
		},
		order: function () {
			opts.order = Utilities.standardizeOrder(Array.prototype.slice.apply(arguments));
			return this;
		},
		select: function () {
			if (arguments.length === 0) {
				throw new ORMError('PARAM_MISMATCH', "When using append you must at least define one property");
			}
			if (Array.isArray(arguments[0])) {
...
```

#### <a name="apidoc.element.orm.Utilities.transformOrderPropertyNames"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>transformOrderPropertyNames (order, properties)](#apidoc.element.orm.Utilities.transformOrderPropertyNames)
- description and source-code
```javascript
transformOrderPropertyNames = function (order, properties) {
	if (!order) return order;

	var i, item;
	var newOrder = JSON.parse(JSON.stringify(order));

	// Rename order properties according to mapsTo
	for (var i = 0; i < newOrder.length; i++) {
		item = newOrder[i];

		// orderRaw
		if (Array.isArray(item[1])) continue;

		if (Array.isArray(item[0])) {
			// order on a hasMany
			// [ ['modelName', 'propName'], 'Z']
			item[0][1] = properties[item[0][1]].mapsTo;
		} else {
			// normal order
			item[0] = properties[item[0]].mapsTo;
		}
	}
	return newOrder;
}
```
- example usage
```shell
...
	var prepareConditions = function () {
		return Utilities.transformPropertyNames(
			opts.conditions, opts.properties
		);
	};

	var prepareOrder = function () {
		return Utilities.transformOrderPropertyNames(
			opts.order, opts.properties
		);
	};

	var chainRun = function (done) {
		var order, conditions;
...
```

#### <a name="apidoc.element.orm.Utilities.transformPropertyNames"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>transformPropertyNames (dataIn, properties)](#apidoc.element.orm.Utilities.transformPropertyNames)
- description and source-code
```javascript
transformPropertyNames = function (dataIn, properties) {
	var k, prop;
	var dataOut = {};

	for (k in dataIn) {
		prop = properties[k];
		if (prop) {
			dataOut[prop.mapsTo] = dataIn[k];
		} else {
			dataOut[k] = dataIn[k];
		}
	}
	return dataOut;
}
```
- example usage
```shell
...
var ChainInstance = require("./ChainInstance");
var Promise       = require("./Promise").Promise;

module.exports = ChainFind;

function ChainFind(Model, opts) {
	var prepareConditions = function () {
		return Utilities.transformPropertyNames(
			opts.conditions, opts.properties
		);
	};

	var prepareOrder = function () {
		return Utilities.transformOrderPropertyNames(
			opts.order, opts.properties
...
```

#### <a name="apidoc.element.orm.Utilities.values"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>values (obj, keys)](#apidoc.element.orm.Utilities.values)
- description and source-code
```javascript
values = function (obj, keys) {
	var i, k, vals = [];

	if (keys) {
		for (i = 0; i < keys.length; i++) {
			vals.push(obj[keys[i]]);
		}
	} else if (Array.isArray(obj)) {
		for (i = 0; i < obj.length; i++) {
			vals.push(obj[i]);
		}
	} else {
		for (k in obj) {
			if (!/[0-9]+/.test(k)) {
				vals.push(obj[k]);
			}
		}
	}
	return vals;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.Utilities.wrapFieldObject"></a>[function <span class="apidocSignatureSpan">orm.Utilities.</span>wrapFieldObject (params)](#apidoc.element.orm.Utilities.wrapFieldObject)
- description and source-code
```javascript
wrapFieldObject = function (params) {
	if (!params.field) {
		var assoc_key = params.model.settings.get("properties.association_key");

		if (typeof assoc_key === "function") {
		    params.field = assoc_key(params.altName.toLowerCase(), params.model.id[0]);
		} else {
			params.field = assoc_key.replace("{name}", params.altName.toLowerCase())
			               .replace("{field}", params.model.id[0]);
		}
	}

	if (typeof params.field == 'object') {
		for (var k in params.field) {
			if (!/[0-9]+/.test(k) && params.field.hasOwnProperty(k)) {
				return params.field;
			}
		}
	}

	var newObj = {}, newProp, propPreDefined, propFromKey;

	propPreDefined = params.model.properties[params.field];
	propFromKey    = params.model.properties[params.model.id[0]];
	newProp        = { type: 'integer' };

	var prop = _.cloneDeep(propPreDefined || propFromKey || newProp);

	if (!propPreDefined) {
		_.extend(prop, {
			name: params.field, mapsTo: params.mapsTo || params.field
		});
	}

	newObj[params.field] = prop;

	return newObj;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.enforce"></a>[module orm.enforce](#apidoc.module.orm.enforce)

#### <a name="apidoc.element.orm.enforce.Enforce"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>Enforce (options)](#apidoc.element.orm.enforce.Enforce)
- description and source-code
```javascript
function Enforce(options) {
    this.validations = {};
    this.contexts = {};
    this.options = {
        returnAllErrors: options && !!options.returnAllErrors
    };

    return this;
}
```
- example usage
```shell
...

		Hook.wait(instance, opts.hooks.beforeValidation, function (err) {
		    var k, i;
			if (err) {
				return saveError(cb, err);
			}

			var checks = new enforce.Enforce({
				returnAllErrors : Model.settings.get("instance.returnAllErrors")
			});

			for (k in opts.validations) {
				required = false;

				if (Model.allProperties[k]) {
...
```

#### <a name="apidoc.element.orm.enforce.Validator"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>Validator (validate)](#apidoc.element.orm.enforce.Validator)
- description and source-code
```javascript
function Validator(validate) {
    this.validator = validate;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.equalToProperty"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>equalToProperty (name, msg)](#apidoc.element.orm.enforce.equalToProperty)
- description and source-code
```javascript
equalToProperty = function (name, msg) {
	return function (v, next) {
		if (v === this[name]) {
			return next();
		}
		return next(msg || 'not-equal-to-property');
	};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.notEmptyString"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>notEmptyString (message)](#apidoc.element.orm.enforce.notEmptyString)
- description and source-code
```javascript
function notEmptyString(message) {
    if (typeof message === "undefined") { message = 'empty-string'; }

    return Ranges.length(1, undefined, message);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.required"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>required (message)](#apidoc.element.orm.enforce.required)
- description and source-code
```javascript
function required(message) {
    if (typeof message === "undefined") { message = 'required'; }

    return new Validator(function (value, next) {
        if (value === null || value === undefined) {
            return next(message);
        }

        return next();
    });
}
```
- example usage
```shell
...
				break;
		}

		allProperties[prop.name]        = prop;
		fieldToPropertyMap[prop.mapsTo] = prop;

		if (prop.required) {
			model.prependValidation(prop.name, Validators.required());
		}

		if (prop.key && prop.klass == 'primary') {
			keyProperties.push(prop);
		}

		if (prop.lazyload !== true && !currFields[prop.name]) {
...
```

#### <a name="apidoc.element.orm.enforce.sameAs"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>sameAs (property, message)](#apidoc.element.orm.enforce.sameAs)
- description and source-code
```javascript
function sameAs(property, message) {
	if (typeof message === "undefined") { message = 'not-same-as'; }

	return new Validator(function (value, next) {
		if (value !== this[property]) {
			return next(message);
		}

		return next();
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.unique"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>unique ()](#apidoc.element.orm.enforce.unique)
- description and source-code
```javascript
unique = function () {
	var arg, k;
	var msg = null, opts = {};

	for (k in arguments) {
		arg = arguments[k];
		if (typeof arg === "string") {
			msg = arg;
		} else if (typeof arg === "object") {
			opts = arg;
		}
	}

	return function (v, next, ctx) {
		var s, scopeProp;

		if (typeof v === "undefined" || v === null) {
			return next();
		}

		//Cannot process on database engines which don't support SQL syntax
		if (!ctx.driver.isSql) {
			return next('not-supported');
		}

		var chain = ctx.model.find();

		var chainQuery = function (prop, value) {
			var query = null;

			if (opts.ignoreCase === true && ctx.model.properties[prop] && ctx.model.properties[prop].type === 'text') {
				query = util.format('LOWER(%s.%s) LIKE LOWER(?)',
					ctx.driver.query.escapeId(ctx.model.table), ctx.driver.query.escapeId(prop)
				);
				chain.where(query, [value]);
			} else {
				query = {};
				query[prop] = value;
				chain.where(query);
			}
		};

		var handler = function (err, records) {
			if (err) {
				return next();
			}
			if (!records || records.length === 0) {
				return next();
			}
			if (records.length === 1 && records[0][ctx.model.id] === this[ctx.model.id]) {
				return next();
			}
			return next(msg || 'not-unique');
		}.bind(this);

		chainQuery(ctx.property, v);

		if (opts.scope) {
			for (s in opts.scope) {
				scopeProp = opts.scope[s];

				// In SQL unique index land, NULL values are not considered equal.
				if (typeof ctx.instance[scopeProp] == 'undefined' || ctx.instance[scopeProp] === null) {
					return next();
				}

				chainQuery(scopeProp, ctx.instance[scopeProp]);
			}
		}

		chain.all(handler);
	};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.enforce.Enforce"></a>[module orm.enforce.Enforce](#apidoc.module.orm.enforce.Enforce)

#### <a name="apidoc.element.orm.enforce.Enforce.Enforce"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>Enforce (options)](#apidoc.element.orm.enforce.Enforce.Enforce)
- description and source-code
```javascript
function Enforce(options) {
    this.validations = {};
    this.contexts = {};
    this.options = {
        returnAllErrors: options && !!options.returnAllErrors
    };

    return this;
}
```
- example usage
```shell
...

		Hook.wait(instance, opts.hooks.beforeValidation, function (err) {
		    var k, i;
			if (err) {
				return saveError(cb, err);
			}

			var checks = new enforce.Enforce({
				returnAllErrors : Model.settings.get("instance.returnAllErrors")
			});

			for (k in opts.validations) {
				required = false;

				if (Model.allProperties[k]) {
...
```



# <a name="apidoc.module.orm.enforce.Enforce.prototype"></a>[module orm.enforce.Enforce.prototype](#apidoc.module.orm.enforce.Enforce.prototype)

#### <a name="apidoc.element.orm.enforce.Enforce.prototype.add"></a>[function <span class="apidocSignatureSpan">orm.enforce.Enforce.prototype.</span>add (property, validator)](#apidoc.element.orm.enforce.Enforce.prototype.add)
- description and source-code
```javascript
add = function (property, validator) {
    if (typeof validator === 'function' && validator.length >= 2) {
        validator = new Validator(validator);
    }

    if (validator.validate === undefined) {
        throw new Error('Missing validator (function) in Enforce.add(property, validator)');
    }

    if (!this.validations.hasOwnProperty(property))
        this.validations[property] = [];

    this.validations[property].push(validator);
    return this;
}
```
- example usage
```shell
...
						}
					}
				}
				if (!alwaysValidate && !required && instance[k] == null) {
					continue; // avoid validating if property is not required and is "empty"
				}
				for (i = 0; i < opts.validations[k].length; i++) {
					checks.add(k, opts.validations[k][i]);
				}
			}

			checks.context("instance", instance);
			checks.context("model", Model);
			checks.context("driver", opts.driver);
...
```

#### <a name="apidoc.element.orm.enforce.Enforce.prototype.check"></a>[function <span class="apidocSignatureSpan">orm.enforce.Enforce.prototype.</span>check (data, cb)](#apidoc.element.orm.enforce.Enforce.prototype.check)
- description and source-code
```javascript
check = function (data, cb) {
    var _this = this;
    var validations = [];

    var errors = [];
    var next = function () {
        if (validations.length === 0) {
            if (errors.length > 0)
                return cb(errors);
else
                return cb(null);
        }

        var validation = validations.shift();
        _this.contexts.property = validation.property;

        validation.validator.validate(data[validation.property], function (message) {
            if (message) {
                var err = new Error(message);
                err.property = validation.property;
                err.value = data[validation.property];
                err.msg = message;
                err.type = "validation";

                if (!this.options.returnAllErrors)
                    return cb(err);
                errors.push(err);
            }

            return next();
        }.bind(_this), data, _this.contexts);
    };

    for (var k in this.validations) {
        for (var i = 0; i < this.validations[k].length; i++) {
            validations.push({
                property: k,
                validator: this.validations[k][i]
            });
        }
    }

    return next();
}
```
- example usage
```shell
...
				}
			}

			checks.context("instance", instance);
			checks.context("model", Model);
			checks.context("driver", opts.driver);

			return checks.check(instance, cb);
		});
	};
	var saveError = function (cb, err) {
		instance_saving = false;

		emitEvent("save", err, instance);
...
```

#### <a name="apidoc.element.orm.enforce.Enforce.prototype.clear"></a>[function <span class="apidocSignatureSpan">orm.enforce.Enforce.prototype.</span>clear ()](#apidoc.element.orm.enforce.Enforce.prototype.clear)
- description and source-code
```javascript
clear = function () {
    this.validations = {};
}
```
- example usage
```shell
...
			done(null, single ? items[0] : items);
		});

		return this;
	};

	model.clear = function (cb) {
		opts.driver.clear(opts.table, function (err) {
			if (typeof cb === "function") cb(err);
		});

		return this;
	};

	model.prependValidation = function (key, validation) {
...
```

#### <a name="apidoc.element.orm.enforce.Enforce.prototype.context"></a>[function <span class="apidocSignatureSpan">orm.enforce.Enforce.prototype.</span>context (name, value)](#apidoc.element.orm.enforce.Enforce.prototype.context)
- description and source-code
```javascript
context = function (name, value) {
    if (name && value) {
        this.contexts[name] = value;
        return this;
    } else if (name)
        return this.contexts[name];
else
        return this.contexts;
}
```
- example usage
```shell
...
					continue; // avoid validating if property is not required and is "empty"
				}
				for (i = 0; i < opts.validations[k].length; i++) {
					checks.add(k, opts.validations[k][i]);
				}
			}

			checks.context("instance", instance);
			checks.context("model", Model);
			checks.context("driver", opts.driver);

			return checks.check(instance, cb);
		});
	};
	var saveError = function (cb, err) {
...
```



# <a name="apidoc.module.orm.enforce.Validator"></a>[module orm.enforce.Validator](#apidoc.module.orm.enforce.Validator)

#### <a name="apidoc.element.orm.enforce.Validator.Validator"></a>[function <span class="apidocSignatureSpan">orm.enforce.</span>Validator (validate)](#apidoc.element.orm.enforce.Validator.Validator)
- description and source-code
```javascript
function Validator(validate) {
    this.validator = validate;
    return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.enforce.Validator.prototype"></a>[module orm.enforce.Validator.prototype](#apidoc.module.orm.enforce.Validator.prototype)

#### <a name="apidoc.element.orm.enforce.Validator.prototype.ifDefined"></a>[function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>ifDefined ()](#apidoc.element.orm.enforce.Validator.prototype.ifDefined)
- description and source-code
```javascript
ifDefined = function () {
    var _this = this;
    return new Validator(function (value, next, contexts) {
        if (value === undefined || value === null)
            return next();
        return _this.validator(value, next, contexts);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.Validator.prototype.ifNotEmptyString"></a>[function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>ifNotEmptyString ()](#apidoc.element.orm.enforce.Validator.prototype.ifNotEmptyString)
- description and source-code
```javascript
ifNotEmptyString = function () {
    var _this = this;
    return new Validator(function (value, next, contexts) {
        if (value === undefined || value === null)
            return next();
        if (typeof value !== 'string')
            return next();
        if (value.length === 0)
            return next();
        return _this.validator(value, next, contexts);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.Validator.prototype.ifNotType"></a>[function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>ifNotType (type)](#apidoc.element.orm.enforce.Validator.prototype.ifNotType)
- description and source-code
```javascript
ifNotType = function (type) {
    var _this = this;
    return new Validator(function (value, next, contexts) {
        if (typeof value != type)
            return _this.validator(value, next, contexts);
        return next();
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.Validator.prototype.ifType"></a>[function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>ifType (type)](#apidoc.element.orm.enforce.Validator.prototype.ifType)
- description and source-code
```javascript
ifType = function (type) {
    var _this = this;
    return new Validator(function (value, next, contexts) {
        if (typeof value != type)
            return next();
        return _this.validator(value, next, contexts);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.Validator.prototype.validate"></a>[function <span class="apidocSignatureSpan">orm.enforce.Validator.prototype.</span>validate (data, next, thisArg, contexts)](#apidoc.element.orm.enforce.Validator.prototype.validate)
- description and source-code
```javascript
validate = function (data, next, thisArg, contexts) {
    if (typeof contexts === "undefined") { contexts = {}; }
    this.validator.apply(thisArg, [data, next, contexts]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.enforce.lists"></a>[module orm.enforce.lists](#apidoc.module.orm.enforce.lists)

#### <a name="apidoc.element.orm.enforce.lists.inside"></a>[function <span class="apidocSignatureSpan">orm.enforce.lists.</span>inside (list, message)](#apidoc.element.orm.enforce.lists.inside)
- description and source-code
```javascript
function inside(list, message) {
    if (typeof message === "undefined") { message = 'outside-list'; }
    return new Validator(function (value, next) {
        if (list.indexOf(value) >= 0)
            return next();
        return next(message);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.lists.outside"></a>[function <span class="apidocSignatureSpan">orm.enforce.lists.</span>outside (list, message)](#apidoc.element.orm.enforce.lists.outside)
- description and source-code
```javascript
function outside(list, message) {
    if (typeof message === "undefined") { message = 'inside-list'; }
    return new Validator(function (value, next) {
        if (list.indexOf(value) === -1)
            return next();
        return next(message);
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.enforce.patterns"></a>[module orm.enforce.patterns](#apidoc.module.orm.enforce.patterns)

#### <a name="apidoc.element.orm.enforce.patterns.email"></a>[function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>email (message)](#apidoc.element.orm.enforce.patterns.email)
- description and source-code
```javascript
function email(message) {
    if (typeof message === "undefined") { message = 'not-valid-email'; }
    return exports.match("^[a-z0-9\\._%\\+\\-]+@[a-z0-9\\.\\-]+\\.[a-z]{2,63}$", "i", message);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.patterns.hexString"></a>[function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>hexString (message)](#apidoc.element.orm.enforce.patterns.hexString)
- description and source-code
```javascript
function hexString(message) {
    if (typeof message === "undefined") { message = 'not-hex-string'; }
    return exports.match("^[a-f0-9]+$", "i", message);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.patterns.ipv4"></a>[function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>ipv4 (message)](#apidoc.element.orm.enforce.patterns.ipv4)
- description and source-code
```javascript
function ipv4(message) {
    if (typeof message === "undefined") { message = 'not-valid-ipv4'; }
    var p1 = "([1-9]|1[0-9][0-9]?|2[0-4][0-9]|25[0-4])";
    var p2 = "([0-9]|1[0-9][0-9]?|2[0-4][0-9]|25[0-4])";
    return exports.match("^" + [p1, p2, p2, p1].join("\\.") + "$", "", message);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.patterns.ipv6"></a>[function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>ipv6 (message)](#apidoc.element.orm.enforce.patterns.ipv6)
- description and source-code
```javascript
function ipv6(message) {
    if (typeof message === "undefined") { message = 'not-valid-ipv6'; }

    var p1 = new RegExp("^([a-f0-9]{1,4}:){7}[a-f0-9]{1,4}$", "i");
    var p2 = new RegExp("^([a-f0-9]{1,4}:)*[a-f0-9]{1,4}$", "i");

    return new Validator(function (value, next) {
        if (typeof value != "string") {
            return next(message);
        }
        // unspecified / loopback
        if ([ "::", "::1" ].indexOf(value) >= 0) {
            return next();
        }
        // normal address (with possible leading zeroes omitted)
        if (value.match(p1)) {
            return next();
        }
        if (value.indexOf("::") == -1) {
            return next(message);
        }
        // grouping zeroes
        var g = value.split("::");

        if (g.length != 2) {
            return next(message);
        }
        if (!g[0].match(p2) || !g[1].match(p2)) {
            return next(message);
        }
        return next();
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.patterns.mac"></a>[function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>mac (message)](#apidoc.element.orm.enforce.patterns.mac)
- description and source-code
```javascript
function mac(message) {
    if (typeof message === "undefined") { message = 'not-valid-mac'; }
    var p = "[0-9a-f]{1,2}";
    var s = "[\\.:]";
    return exports.match("^" + [p,p,p,p,p,p].join(s) + "$", "i", message);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.patterns.match"></a>[function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>match (pattern, modifiers, message)](#apidoc.element.orm.enforce.patterns.match)
- description and source-code
```javascript
function match(pattern, modifiers, message) {
    if (typeof modifiers === "undefined") { modifiers = 'i'; }
    if (typeof message === "undefined") { message = 'no-pattern-match'; }
    if (arguments.length == 2) {
        message = modifiers;
        modifiers = 'i';
    }

    if (typeof pattern === 'string') {
        pattern = new RegExp(pattern, modifiers);
    }

    return new Validator(function (value, next) {
        if (typeof value === 'string' && value.match(pattern))
            return next();
        return next(message);
    });
}
```
- example usage
```shell
...

exports.getRealPath = function (path_str, stack_index) {
	var path = require("path"); // for now, load here (only when needed)
	var cwd = process.cwd();
	var err = new Error();
	var tmp = err.stack.split(/\r?\n/)[typeof stack_index !== "undefined" ? stack_index : 3], m;

	if ((m = tmp.match(/^\s*at\s+(.+):\d+:\d+$/)) !== null) {
		cwd = path.dirname(m[1]);
	} else if ((m = tmp.match(/^\s*at\s+module\.exports\s+\((.+?)\)/)) !== null) {
		cwd = path.dirname(m[1]);
	} else if ((m = tmp.match(/^\s*at\s+.+\s+\((.+):\d+:\d+\)$/)) !== null) {
		cwd = path.dirname(m[1]);
	}
	var pathIsAbsolute = path.isAbsolute || require('path-is-absolute');
...
```

#### <a name="apidoc.element.orm.enforce.patterns.uuid3"></a>[function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>uuid3 (message)](#apidoc.element.orm.enforce.patterns.uuid3)
- description and source-code
```javascript
function uuid3(message) {
    if (typeof message === "undefined") { message = 'not-valid-uuid3'; }
    return exports.match("^[a-f0-9]{8}\-[a-f0-9]{4}\-3[a-f0-9]{3}\-[89ab][a-f0-9]{3}\-[a-f0-9]{12}$", "i", message);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.patterns.uuid4"></a>[function <span class="apidocSignatureSpan">orm.enforce.patterns.</span>uuid4 (message)](#apidoc.element.orm.enforce.patterns.uuid4)
- description and source-code
```javascript
function uuid4(message) {
    if (typeof message === "undefined") { message = 'not-valid-uuid4'; }
    return exports.match("^[a-f0-9]{8}\-[a-f0-9]{4}\-4[a-f0-9]{3}\-[89ab][a-f0-9]{3}\-[a-f0-9]{12}$", "i", message);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.enforce.ranges"></a>[module orm.enforce.ranges](#apidoc.module.orm.enforce.ranges)

#### <a name="apidoc.element.orm.enforce.ranges.length"></a>[function <span class="apidocSignatureSpan">orm.enforce.ranges.</span>length (min, max, message)](#apidoc.element.orm.enforce.ranges.length)
- description and source-code
```javascript
function length(min, max, message) {
    if (typeof message === "undefined") { message = 'out-of-range-length'; }
    return new Validator(function (value, next) {
        if (value === undefined || value === null)
            return next('undefined');
        if (min === undefined && value.length <= max)
            return next();
        if (max === undefined && value.length >= min)
            return next();
        if (value.length >= min && value.length <= max)
            return next();
        return next(message);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.ranges.number"></a>[function <span class="apidocSignatureSpan">orm.enforce.ranges.</span>number (min, max, message)](#apidoc.element.orm.enforce.ranges.number)
- description and source-code
```javascript
function number(min, max, message) {
    if (typeof message === "undefined") { message = 'out-of-range-number'; }
    return new Validator(function (value, next) {
        if (value === undefined || value === null)
            return next('undefined');
        if (min === undefined && value <= max)
            return next();
        if (max === undefined && value >= min)
            return next();
        if (value >= min && value <= max)
            return next();
        return next(message);
    });
}
```
- example usage
```shell
...
	}, {
		methods: {
			fullName: function () {
				return this.name + ' ' + this.surname;
			}
		},
		validations: {
			age: orm.enforce.ranges.number(18, undefined, "under-age")
		}
	});

    // add the table to the database
	db.sync(function(err) {
		if (err) throw err;
...
```



# <a name="apidoc.module.orm.enforce.security"></a>[module orm.enforce.security](#apidoc.module.orm.enforce.security)

#### <a name="apidoc.element.orm.enforce.security.creditcard"></a>[function <span class="apidocSignatureSpan">orm.enforce.security.</span>creditcard (types, message)](#apidoc.element.orm.enforce.security.creditcard)
- description and source-code
```javascript
function creditcard(types, message) {
    if (typeof types === "undefined") { types = ["amex", "visa", "maestro", "discover", "mastercard"]; }
    if (typeof message === "undefined") { message = 'not-valid-creditcard'; }
    return new Validator(function (v, next) {
        if (!v)
            return next(message);

        v = "" + v;

        var ok = false;

        for (var i = 0; i < types.length; i++) {
            switch (types[i]) {
                case "amex":
                    if (v.length != 15)
                        break;

                    ok = (creditcard_prefixes["amex"].indexOf(v.substr(0, 2)) >= 0);
                    break;
                case "visa":
                    if (v.length < 13)
                        break;
                    if (v.length > 16)
                        break;

                    ok = (v[0] == "4");
                    break;
                case "maestro":
                    if (v.length < 16)
                        break;
                    if (v.length > 19)
                        break;

                    ok = (creditcard_prefixes["maestro"].indexOf(v.substr(0, 4)) >= 0);
                    break;
                case "mastercard":
                    if (v.length < 16)
                        break;
                    if (v.length > 19)
                        break;

                    ok = (creditcard_prefixes["mastercard"].indexOf(v.substr(0, 2)) >= 0);
                    break;
                case "discover":
                    if (v.length != 16)
                        break;

                    ok = (creditcard_prefixes["discover4"].indexOf(v.substr(0, 4)) >= 0) || (creditcard_prefixes["discover3"].indexOf
(v.substr(0, 3)) >= 0) || (creditcard_prefixes["discover2"].indexOf(v.substr(0, 2)) >= 0);

                    if (!ok) {
                        var prefix = +v.substr(0, 6);

                        ok = (!isNaN(prefix) && prefix >= 622126 && prefix <= 622925);
                    }
                    break;
                case "luhn":
                    // fallback
                    ok = true;
                    break;
            }
            if (ok)
                break;
        }

        if (!ok) {
            return next(message);
        }

        // it's in one of possible types, let's check Luhn
        var check = +v[v.length - 1];

        if (isNaN(check)) {
            return next(message);
        }

        var digits = v.slice(0, v.length - 1).split('');
        digits.reverse();

        for (var i = 0; i < digits.length; i++) {
            digits[i] = +digits[i];
            if (isNaN(digits[i])) {
                return next(message);
            }

            if (i % 2 === 0) {
                digits[i] *= 2;
                if (digits[i] > 9) {
                    digits[i] -= 9;
                }
            }
        }

        check += digits.reduce(function (a, b) {
            return a + b;
        });

        return next(check % 10 !== 0 ? message : null);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.security.password"></a>[function <span class="apidocSignatureSpan">orm.enforce.security.</span>password (checks, message)](#apidoc.element.orm.enforce.security.password)
- description and source-code
```javascript
function password(checks, message) {
    if (!message) {
        message = checks;
        checks = "luns6";
    }

    if (!message) {
        message = "weak-password";
    }

    var m = checks.match(/([0-9]+)/);
    var min_len = (m ? parseInt(m[1], 10) : null);

    return new Validator(function (value, next) {
        if (!value)
            return next(message);

        if (checks.indexOf("l") >= 0 && !value.match(/[a-z]/))
            return next(message);
        if (checks.indexOf("u") >= 0 && !value.match(/[A-Z]/))
            return next(message);
        if (checks.indexOf("n") >= 0 && !value.match(/[0-9]/))
            return next(message);
        if (checks.indexOf("s") >= 0 && !value.match(/[^a-zA-Z0-9]/))
            return next(message);
        if (min_len !== null && min_len > value.length)
            return next(message);

        return next();
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.enforce.security.username"></a>[function <span class="apidocSignatureSpan">orm.enforce.security.</span>username (options, message)](#apidoc.element.orm.enforce.security.username)
- description and source-code
```javascript
function username(options, message) {
    if (typeof options === "undefined") { options = { length: 2, expr: null }; }
    if (typeof message === "undefined") { message = 'invalid-username'; }
    if (typeof options === 'string') {
        message = options.toString();
        options = { length: 2, expr: null };
    }

    if (!options.expr) {
        options.expr = new RegExp("^[a-z_][a-z0-9_\\-]{" + (options.length - 1) + ",}$", "i");
    }

    return patterns.match(options.expr, message);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.settings"></a>[module orm.settings](#apidoc.module.orm.settings)

#### <a name="apidoc.element.orm.settings.get"></a>[function <span class="apidocSignatureSpan">orm.settings.</span>get (key, def)](#apidoc.element.orm.settings.get)
- description and source-code
```javascript
get = function (key, def) {
			var v = get(key, def, settings)

			if (v instanceof Function) {
				return v;
			} else {
				return _.cloneDeep(v);
			}
		}
```
- example usage
```shell
...
	define: function (db, models, next) {
		models.person = db.define("person", { ... });
		next();
	}
}));
app.listen(80);

app.get("/", function (req, res) {
	// req.models is a reference to models used above in define()
	req.models.person.find(...);
});
'''

You can call 'orm.express' more than once to have multiple database connections. Models defined across connections
will be joined together in 'req.models'. **Don't forget to use it before 'app.use(app.router)', preferably right after your
...
```

#### <a name="apidoc.element.orm.settings.set"></a>[function <span class="apidocSignatureSpan">orm.settings.</span>set (key, value)](#apidoc.element.orm.settings.set)
- description and source-code
```javascript
set = function (key, value) {
			set(key, value, settings);

			return this;
		}
```
- example usage
```shell
...
'''js
var Person = db.define("person", {
	personId : { type: 'serial', key: true },
	name     : String
});

// You can also change the default "id" property name globally:
db.settings.set("properties.primary_key", "UID");

// ..and then define your Models
var Pet = db.define("pet", {
	name : String
});
'''
...
```

#### <a name="apidoc.element.orm.settings.unset"></a>[function <span class="apidocSignatureSpan">orm.settings.</span>unset ()](#apidoc.element.orm.settings.unset)
- description and source-code
```javascript
unset = function () {
			for (var i = 0; i < arguments.length; i++) {
				if (typeof arguments[i] === "string") {
					unset(arguments[i], settings);
				}
			}

			return this;
		}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.orm.singleton"></a>[module orm.singleton](#apidoc.module.orm.singleton)

#### <a name="apidoc.element.orm.singleton.clear"></a>[function <span class="apidocSignatureSpan">orm.singleton.</span>clear (key)](#apidoc.element.orm.singleton.clear)
- description and source-code
```javascript
clear = function (key) {
	if (typeof key === "string") {
		delete map[key];
	} else {
		map = {};
	}
	return this;
}
```
- example usage
```shell
...
			done(null, single ? items[0] : items);
		});

		return this;
	};

	model.clear = function (cb) {
		opts.driver.clear(opts.table, function (err) {
			if (typeof cb === "function") cb(err);
		});

		return this;
	};

	model.prependValidation = function (key, validation) {
...
```

#### <a name="apidoc.element.orm.singleton.get"></a>[function <span class="apidocSignatureSpan">orm.singleton.</span>get (key, opts, createCb, returnCb)](#apidoc.element.orm.singleton.get)
- description and source-code
```javascript
get = function (key, opts, createCb, returnCb) {
	if (opts && opts.identityCache === false) {
		return createCb(returnCb);
	}
	if (map.hasOwnProperty(key)) {
		if (opts && opts.saveCheck && typeof map[key].o.saved === "function" && !map[key].o.saved()) {
			// if not saved, don't return it, fetch original from db
			return createCb(returnCb);
		} else if (map[key].t !== null && map[key].t <= Date.now()) {
			delete map[key];
		} else  {
			return returnCb(null, map[key].o);
		}
	}

	createCb(function (err, value) {
		if (err) return returnCb(err);

		map[key] = { // object , timeout
			o : value,
			t : (opts && typeof opts.identityCache === "number" ? Date.now() + (opts.identityCache * 1000) : null)
		};
		return returnCb(null, map[key].o);
	});
}
```
- example usage
```shell
...
	define: function (db, models, next) {
		models.person = db.define("person", { ... });
		next();
	}
}));
app.listen(80);

app.get("/", function (req, res) {
	// req.models is a reference to models used above in define()
	req.models.person.find(...);
});
'''

You can call 'orm.express' more than once to have multiple database connections. Models defined across connections
will be joined together in 'req.models'. **Don't forget to use it before 'app.use(app.router)', preferably right after your
...
```



# <a name="apidoc.module.orm.validators"></a>[module orm.validators](#apidoc.module.orm.validators)

#### <a name="apidoc.element.orm.validators.equalToProperty"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>equalToProperty (name, msg)](#apidoc.element.orm.validators.equalToProperty)
- description and source-code
```javascript
equalToProperty = function (name, msg) {
	return function (v, next) {
		if (v === this[name]) {
			return next();
		}
		return next(msg || 'not-equal-to-property');
	};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.validators.insideList"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>insideList (list, message)](#apidoc.element.orm.validators.insideList)
- description and source-code
```javascript
function inside(list, message) {
    if (typeof message === "undefined") { message = 'outside-list'; }
    return new Validator(function (value, next) {
        if (list.indexOf(value) >= 0)
            return next();
        return next(message);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.validators.notEmptyString"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>notEmptyString (message)](#apidoc.element.orm.validators.notEmptyString)
- description and source-code
```javascript
function notEmptyString(message) {
    if (typeof message === "undefined") { message = 'empty-string'; }

    return Ranges.length(1, undefined, message);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.validators.outsideList"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>outsideList (list, message)](#apidoc.element.orm.validators.outsideList)
- description and source-code
```javascript
function outside(list, message) {
    if (typeof message === "undefined") { message = 'inside-list'; }
    return new Validator(function (value, next) {
        if (list.indexOf(value) === -1)
            return next();
        return next(message);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.validators.password"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>password (checks, message)](#apidoc.element.orm.validators.password)
- description and source-code
```javascript
function password(checks, message) {
    if (!message) {
        message = checks;
        checks = "luns6";
    }

    if (!message) {
        message = "weak-password";
    }

    var m = checks.match(/([0-9]+)/);
    var min_len = (m ? parseInt(m[1], 10) : null);

    return new Validator(function (value, next) {
        if (!value)
            return next(message);

        if (checks.indexOf("l") >= 0 && !value.match(/[a-z]/))
            return next(message);
        if (checks.indexOf("u") >= 0 && !value.match(/[A-Z]/))
            return next(message);
        if (checks.indexOf("n") >= 0 && !value.match(/[0-9]/))
            return next(message);
        if (checks.indexOf("s") >= 0 && !value.match(/[^a-zA-Z0-9]/))
            return next(message);
        if (min_len !== null && min_len > value.length)
            return next(message);

        return next();
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.validators.rangeLength"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>rangeLength (min, max, message)](#apidoc.element.orm.validators.rangeLength)
- description and source-code
```javascript
function length(min, max, message) {
    if (typeof message === "undefined") { message = 'out-of-range-length'; }
    return new Validator(function (value, next) {
        if (value === undefined || value === null)
            return next('undefined');
        if (min === undefined && value.length <= max)
            return next();
        if (max === undefined && value.length >= min)
            return next();
        if (value.length >= min && value.length <= max)
            return next();
        return next(message);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.validators.rangeNumber"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>rangeNumber (min, max, message)](#apidoc.element.orm.validators.rangeNumber)
- description and source-code
```javascript
function number(min, max, message) {
    if (typeof message === "undefined") { message = 'out-of-range-number'; }
    return new Validator(function (value, next) {
        if (value === undefined || value === null)
            return next('undefined');
        if (min === undefined && value <= max)
            return next();
        if (max === undefined && value >= min)
            return next();
        if (value >= min && value <= max)
            return next();
        return next(message);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.orm.validators.required"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>required (message)](#apidoc.element.orm.validators.required)
- description and source-code
```javascript
function required(message) {
    if (typeof message === "undefined") { message = 'required'; }

    return new Validator(function (value, next) {
        if (value === null || value === undefined) {
            return next(message);
        }

        return next();
    });
}
```
- example usage
```shell
...
				break;
		}

		allProperties[prop.name]        = prop;
		fieldToPropertyMap[prop.mapsTo] = prop;

		if (prop.required) {
			model.prependValidation(prop.name, Validators.required());
		}

		if (prop.key && prop.klass == 'primary') {
			keyProperties.push(prop);
		}

		if (prop.lazyload !== true && !currFields[prop.name]) {
...
```

#### <a name="apidoc.element.orm.validators.unique"></a>[function <span class="apidocSignatureSpan">orm.validators.</span>unique ()](#apidoc.element.orm.validators.unique)
- description and source-code
```javascript
unique = function () {
	var arg, k;
	var msg = null, opts = {};

	for (k in arguments) {
		arg = arguments[k];
		if (typeof arg === "string") {
			msg = arg;
		} else if (typeof arg === "object") {
			opts = arg;
		}
	}

	return function (v, next, ctx) {
		var s, scopeProp;

		if (typeof v === "undefined" || v === null) {
			return next();
		}

		//Cannot process on database engines which don't support SQL syntax
		if (!ctx.driver.isSql) {
			return next('not-supported');
		}

		var chain = ctx.model.find();

		var chainQuery = function (prop, value) {
			var query = null;

			if (opts.ignoreCase === true && ctx.model.properties[prop] && ctx.model.properties[prop].type === 'text') {
				query = util.format('LOWER(%s.%s) LIKE LOWER(?)',
					ctx.driver.query.escapeId(ctx.model.table), ctx.driver.query.escapeId(prop)
				);
				chain.where(query, [value]);
			} else {
				query = {};
				query[prop] = value;
				chain.where(query);
			}
		};

		var handler = function (err, records) {
			if (err) {
				return next();
			}
			if (!records || records.length === 0) {
				return next();
			}
			if (records.length === 1 && records[0][ctx.model.id] === this[ctx.model.id]) {
				return next();
			}
			return next(msg || 'not-unique');
		}.bind(this);

		chainQuery(ctx.property, v);

		if (opts.scope) {
			for (s in opts.scope) {
				scopeProp = opts.scope[s];

				// In SQL unique index land, NULL values are not considered equal.
				if (typeof ctx.instance[scopeProp] == 'undefined' || ctx.instance[scopeProp] === null) {
					return next();
				}

				chainQuery(scopeProp, ctx.instance[scopeProp]);
			}
		}

		chain.all(handler);
	};
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

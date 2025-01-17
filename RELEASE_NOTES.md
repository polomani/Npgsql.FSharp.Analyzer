### 3.24.0 - 2021-04-09
* fixes dynamically applied parameters with more complex expressions 

### 3.23.0 - 2021-03-26
* Detect typed let bindings 

### 3.22.1 - 2021-02-09
* Let the analyzer continue its work when it comes across enum types 

### 3.22.0 - 2020-12-08
* Detect queries within sequential expressions or statements

### 3.21.0 - 2020-12-08
* Detect queries within lambda expressions wrapped in single case unions

### 3.20.0 - 2020-12-08
* Correctly retain selected column non-nullability when casted or aliased to another type

### 3.18.0 - 2020-12-06
* Analyze SQL blocks from within lambda expressions

### 3.17.0 - 2020-12-06
* Support for datetimeOffset and datetimeOffsetOrNone when reading columns of type timestamptz

### 3.16.0 - 2020-12-06
* Analyze top level do expressions

### 3.15.0 - 2020-09-15
* Analyze transaction parameter sets 
* Allow for literal queries on transactions

### 3.14.0 - 2020-09-07
* Analyze transaction queries

### 3.13.0 - 2020-09-04
* The ability to suppress warning messages generated by the analyzer

### 3.12.1 - 2020-08-31
* Remove NpgsqlFSharpAnalyzer.Core nuget package reference from the analyzer

### 3.12.0 - 2020-08-29
* Parameter nullability inference for parsable queries
* Detecting the missing columns which are required for INSERT queries
* Better error messages when reading from a result set which doesn't return any columns

### 3.11.0 - 2020-08-18
* Even better error messages that include whether types were arrays or not

#### 3.10.0 - 2020-08-18
* Better error messages when showing the possible functions to use.
* Warning when using Sql.execute and the query doesn't return a result set
* Support for text int and uuid arrays both when reading columns and writing parameters

#### 3.9.0 - 2020-07-19
* Updated FSharp.Analyzers.SDK to 0.5.0

#### 3.8.0 - 2020-06-26
* Trim whitespace from parameter names
* Fix aggressive syntactic matching

#### 3.7.0 - 2020-05-19
* Account for parameters of type `jsonb` and provide proper type mismatch error.

#### 3.6.0 - 2020-05-19
* Add Sql.executeRow(Async) and Sql.iter(Async) to the analysis

#### 3.5.0 - 2020-05-19
* Expand syntactic analysis to include searching through (async) computation expressions

#### 3.4.0 - 2020-05-19
* Search through nested modules and nested recursively
* Configure the connection string of the analyzer via a local file

#### 3.3.0 - 2020-04-17
* Update FSharp.Analyzers SDK 0.4.0 -> 0.4.1

#### 3.2.0 - 2020-03-05
* Update FSharp.Analyzers SDK 0.3.1 -> 0.4.0 with named analyzers.

#### 3.1.0 - 2020-03-05
* Update FSharp.Analyzers SDK and compiler services to align types.

#### 3.0.0 - 2020-02-26
* Update for Npgsql.FSharp 3.x to be able to analyze column reading functions as `{type}OrNone` instead of `{type}OrNull`

#### 2.0.0 - 2020-02-24
* Update for Npgsql.FSharp 2.x
* Detect incorrect parameter type with code fixes
* Detect redundant parameters
* Detect nullable types and and suggest using proper function that handle null values

#### 1.9.0 - 2020-02-20
* Optimize number of database calls by reusing the database schema on each invokation
* Detect redundant query parameters in a clear warning message
* Provide code fixes and better suggestions for mismatched query parameters
* Remove duplicate messages about missing parameters
* Refactor and simplify parts of `InformatioSchema` and `SqlAnalysis`

#### 1.8.0 - 2020-02-19
* Provide column name fix suggestions when reading an unknown column

#### 1.7.0 - 2020-02-19
* Read parameters as soon as they written and implement proper code fixes.

#### 1.6.0 - 2020-02-19
* Read queries as soon as they written without expecting `Sql.executeReader`

#### 1.5.0 - 2020-02-19
* Improved syntactic F# analysis in `Sql` module is used in combination with other generic functions

#### 1.4.0 - 2020-02-18
* Enable reading `[<Literal>]` queries from the same module and add docs

#### 1.3.0 - 2020-02-18
* Detect type-mismatch when reading columns of type 'bool' from the database. Simplify parameter mismatch when there is only one parameter.

#### 1.2.0 - 2020-02-18
* Remove warning when there is no query provided (to avoid making a bother-ware analyzer)

#### 1.1.0 - 2020-02-17
* Proper packaging that includes third-party dependencies required for dynamic loading

#### 1.0.0 - 2020-02-17
* Initial release with working SQL analysis including syntax and type-checking

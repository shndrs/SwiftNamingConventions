# NamingConventions

[![Build Status](https://travis-ci.org/Acidmanic/SwiftNamingConventions.svg?branch=master)](https://travis-ci.org/Acidmanic/SwiftNamingConventions)
[![Version](https://img.shields.io/cocoapods/v/NamingConventions.svg?style=flat)](https://cocoapods.org/pods/NamingConventions)
[![GitHub license](https://img.shields.io/github/license/Acidmanic/SwiftNamingConventions.svg)](https://github.com/Acidmanic/SwiftNamingConventions/blob/master/LICENSE)
[![Platform](https://img.shields.io/cocoapods/p/NamingConventions.svg?style=flat)](https://cocoapods.org/pods/NamingConventions)

<img src="https://raw.githubusercontent.com/Carthage/Carthage/master/Logo/PNG/colored.png" width="32px" height="32px" />  <img src="https://raw.githubusercontent.com/CocoaPods/shared_resources/master/img/CocoaPods-Logo-Highlight.png" width="128px" height="32px" />




About
====

NamingConventions is a library amied to help converting Name/IDs following different Naming Conventinos to each other. for example you might have a string with a given or even unknown naming-convention, and you want it to be converted to say a snake-cased-string. 

Example
=====

To use the code, you will just create an instance of **ConventionConverter** class, call the method: *autoConvert(from:&lt;name-id-string&gt;,to:&lt;destination-convention&gt;)*. and the result will be your string following the destination naming convention.


```swift
	let converter = ConventionConverter()
	let convention = NamingConventions.SnakeCase
	let src = "MyFieldName"
	let result = converter.autoConvert(from: src, to: convention)
	print(src + " -> " + result)
```
output:

```bash
	MyFieldName -> my-field-name
```


**NamingConvention**:

You can get an object of a naming convention from the class: **NamingConventions**. you also can create one using its initializer (constructor) like: 
```swift
 let myConvention = NamingConvention(starter: "_", firstParticle: ParticleCase.Lower, otherParticles: ParticleCase.Pretty, separator: "")
 
```


## Requirements

This project does not have any dependencies (except for foundation!)

## Installation

*	Cocoapods

NamingConventions is available through [CocoaPods](https://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'NamingConventions'
```

*	Carthage

To get the latest version of library using Carthage, you can add following line to your Cartfile.

```bash
github "Acidmanic/SwiftNamingConventions"
```


## License

NamingConventions is available under the MIT license. See the LICENSE file for more info.


Thanks & Good luck 👍
[Mani](https://about.me/moayedi)
<!--

WARNING!! DON'T EDIT THE FILE README.md on the root of the project, that one is a GENERATED FILE!

You should just edit the source file at src/README.md - the one which stars with ## Swagger - Documenting your REST APIs 

-->

## Swagger - Documenting your REST APIs

Swagger language for REST APIs documentations

<img src="img/cover.png" class="logo" />

&lt;/Arlindo Neto&gt; @ [AvenueCode](http://www.avenuecode.com)

*aneto@avenuecode.com*

Dec 8th, 2015

---

## What is Swagger

Swagger is the most popular language to manage REST APIs documentation. 

Besides that, the document itself can be used to mock servers for testing and early stage developmento of a digital product, making it easier to handle pre-MVP applications that can be used to show its concepts to an intereted part.

Other languages available for the same purpose, or almost that, are RAML, mantained by MuleSoft, and the API Bluprint, maintaned by Apiary.

---

## Why Use Swagger

1. Because it is completely based on the Community and not on an industry.
2. Because it has awesome and easy to use tools.
3. Because I like it (my talk, my rules! LOL)

---

## How to use it

There is no need to use any of the tools for creating Swagger documents, but it could be hard to validate its contents without a proper editor.

For that reason, Swagger community created a really good editor that shows the results and warnings/errors in real time, during the edition stage.

Another thing is that, given you would want to secure the source code, the Swagger community also provide us with a simple document browser, allowing any one to see the rendered document, but not the code behind it.

---

## Online Editor

The editor can be accessed with the given URL:

```http://editor.swagger.io/```

This editor, even hosted by an cloud server, allows you to download the current file and also saves its content in the localstorage each time you change the content.

---

## Local Editor

For those who want to have a totally private environment, the project is available on GITHUB. 

You just need to clone the project and run ***npm start*** on its root folder.

```git clone https://github.com/swagger-api/swagger-editor.git```

---

## Specification

All you need to know about Swagger is available on its Specification Docs, on the bellow URL:

```http://swagger.io/specification```

But I will step through some basic stuffs. Don't worry!

---

## Syntax

Swagger uses YML syntax or JSON syntax. 

I suggest use YML, if you know how to do it, becuase of a single limitation of Swagger, comparing with RAML: 

> There is no modularization!

This way the file can become huge with time and YML save you from a too much large file.

---

## Common Sections

The document is splited in some sections where we can define specific objects. We are going to work with just some of them:

- paths
- parameters
- definitions

---

## Document Header

```
swagger: '2.0'
info:
  version: 1.0.0
  title: APIs Backend
host: api.avenuecode.com
schemes:
  - http
  - https
basePath: /api/v1
``` 

As any document we expect to be processed by an engine (for mock servers), we must define some meta data about its content.

The header section contains elements that describe some _background_ information (a Gherkin term) about the contents on the ***paths*** section, like where and how to access its contents, and some informations about the file itself, like version, its title, and the language version for the engine.

---

## Paths Section

As you may know, REST APIs are mostly defined as web resources mapped by its paths on an specified domain (not just that, but...). 

This way, the path is of the resource is the most important thing about it and all that matters about its documentation, is related to it.

A path section is mostly defined by the parameters in the next box.

---

## Path

```
paths:
	/[path]:
		[method]:
			description: [description]
			consumes:
				- [mime type]
				- [...]
			produces:
				- [mime type]
				- [...]
			parameters:
				- [parameter]
				- [...]
			responses:
				[code]:
					description: [description]
					schema:
						[schema]
		[method]:
			...
	/[path]:
		...
```

---

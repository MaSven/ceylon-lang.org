---
layout: reference13
title_md: '`^` (power) operator'
tab: documentation
unique_id: docspage
author: Tom Bentley
doc_root: ../../..
---

# #{page.title_md}

The right-associative, binary infix `^` operator is used to compute its left-hand 
operand *raised to the power* of its right-hand operand.

## Usage 

<!-- try: -->
    Integer eight = 2 ^ 3;

## Description

### Definition

The `^` operator is defined as follows:

<!-- check:none -->
<!-- try: -->
    lhs.power(rhs);

See the [language specification](#{site.urls.spec_current}#arithmetic) for more details.

### Polymorphism

The `^` operator is [polymorphic](#{page.doc_root}/reference/operator/operator-polymorphism). 
The meaning of `^` depends on the 
[`Exponentiable`](#{site.urls.apidoc_1_3}/Exponentiable.type.html) interface.

### Type

The result type of the `^` operator is the same as the type of the `This` type argument of its left hand 
`Exponentiable<This, Other>` operand.

### Meaning of power for built-in types

For the built-in numeric types [`Integer`](#{site.urls.apidoc_1_3}/Integer.type.html) and
[`Float`](#{site.urls.apidoc_1_3}/Float.type.html), `^` 
performs normal mathematical exponentiation, subject to the limitations
of the relevant type.


## See also

* API documentation for [`Exponentiable`](#{site.urls.apidoc_1_3}/Exponentiable.type.html)
* [arithmetic operators](#{site.urls.spec_current}#arithmetic) in the 
  language specification
* [operator precedence](#{site.urls.spec_current}#operatorprecedence) in the 
  language specification
* [Operator polymorphism](#{page.doc_root}/tour/language-module/#operator_polymorphism) 
  and 
  [Numeric operator semantics](#{page.doc_root}/tour/language-module/#numeric_operator_semantics) 
  in the Tour of Ceylon

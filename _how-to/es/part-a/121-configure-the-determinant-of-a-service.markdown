---
layout: recipe
permalink: /como/añadir-un-nuevo-campo-en-la-guia/
title: 'Añadir un nuevo campo en la guía'
category: '1. Part A'
sub-category: 'Determinantes'
rate: '2'
number: '121'
introduction-text: ''
introduction-img: '106.png'
prevUrl: 113
nextUrl: 121
done: ''
lang: es
ref: 121
---

To acomplish this task we need two things:

1. A field in the model
2. Entry in the guide section

To define the field:

1. Open file `model/<business-process-your-service>/fields.js`.
2. Add new definition on `<BusinessProcessYourService>.prototype` (e.g. `myField: { type: db.Boolean, label: _("My field name", required: true }` )).

After the new field is defined, include the new field in the guide section:

1. Open file `model/<business-process-your-service>/guide.js`.
2. Add your field's name to the `propertyNames` property of the `determinants` section (e.g. `propertyNames: ['myField']`).

### Example

Starting Branch: [configure-the-determinant-of-a-service](https://github.com/egovernment/eregistrations-demo/tree/configure-the-determinant-of-a-service)

Let's add a new determinant to the guide.

#### characteristics of the new field:

1. Name: `isLocalInvestment`.
2. Label: "Is the investment local?".
3. Type: `Boolean` (dbjs).
4. Is `required`.

The field should be included in the guide's form as the last property.

[Solution](https://github.com/egovernment/eregistrations-demo/compare/configure-the-determinant-of-a-service...configure-the-determinant-of-a-service-solution?expand=1)

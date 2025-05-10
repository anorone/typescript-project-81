### Hexlet tests and linter status

[![Actions Status](https://github.com/anorone/typescript-project-81/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/anorone/typescript-project-81/actions)
[![Actions Status](https://github.com/anorone/typescript-project-81/actions/workflows/quality-check.yml/badge.svg)](https://github.com/anorone/typescript-project-81/actions/workflows/quality-check.yml)
[![Maintainability](https://qlty.sh/badges/3f5857b1-b09f-41d5-8ba7-973d3745ce02/maintainability.svg)](https://qlty.sh/gh/anorone/projects/typescript-project-81)
[![Code Coverage](https://qlty.sh/badges/3f5857b1-b09f-41d5-8ba7-973d3745ce02/test_coverage.svg)](https://qlty.sh/gh/anorone/projects/typescript-project-81)

## Description

Form Generator is a library that allows to create html forms in website templates.

## Example

```javascript
import FormGenerator from '@hexlet/code';

const template = {
  name: 'anna',
  job: 'nurse',
  gender: 'f',
};

const form = FormGenerator.formFor(template, { method: 'post' }, (f) => {
  f.input('name');
  f.input('job', { as: 'textarea' });
  f.submit();
});

console.log(form);

//  <form action="#" method="post">
//    <label for="name">Name</label>
//    <input id="name" name="name" type="text" value="anna">
//    <label for="job">Job</label>
//    <textarea cols="20" rows="40" id="job" name="job">nurse</textarea>
//    <input type="submit" value="Save">
//  </form>
```

___
**Note du traducteur**

C'est la traduction du fichier [no-identical-title.md](https://github.com/avajs/eslint-plugin-ava/blob/master/docs/rules/no-identical-title.md). Voici un [lien](https://github.com/avajs/eslint-plugin-ava/compare/7542453058c30ebbc79c7bfeb689492fce226d8f...main#diff-71a0207aeafb9ca6c33c3d06982b1baa) vers les différences avec le master de eslint-plugin-ava (Si en cliquant sur le lien, vous ne trouvez pas le fichier `no-identical-title.md` parmi les fichiers modifiés, vous pouvez donc en déduire que la traduction est à jour).
___
# S'assurer que chaque test a un titre différent

Traductions : [English](https://github.com/avajs/eslint-plugin-ava/blob/master/docs/rules/no-identical-title.md)

Interdit les tests avec des titres identiques car il est difficile de les différencier.


## Échoue

```js
const test = require('ava');

test('foo', t => {
	t.pass();
});

test('foo', t => {
	t.pass();
});
```


## Passe

```js
const test = require('ava');

test(t => {
	t.pass();
});

test('foo', t => {
	t.pass();
});

test('bar', t => {
	t.pass();
});
```

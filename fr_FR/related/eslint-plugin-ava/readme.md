___
**Note du traducteur**

C'est la traduction du fichier [readme.md](https://github.com/avajs/eslint-plugin-ava/blob/master/readme.md). Voici un [lien](https://github.com/avajs/eslint-plugin-ava/compare/1b1986c3b29b8edb08b54881b5c31df678a67871...master#diff-0730bb7c2e8f9ea2438b52e419dd86c9) vers les différences avec le master de eslint-plugin-ava (Si en cliquant sur le lien, vous ne trouvez pas le fichier `readme.md` parmi les fichiers modifiés, vous pouvez donc en déduire que la traduction est à jour).
___
# eslint-plugin-ava [![Build Status](https://travis-ci.org/avajs/eslint-plugin-ava.svg?branch=master)](https://travis-ci.org/avajs/eslint-plugin-ava) [![Coverage Status](https://coveralls.io/repos/github/avajs/eslint-plugin-ava/badge.svg?branch=master)](https://coveralls.io/github/avajs/eslint-plugin-ava?branch=master)

> Règles ESLint pour [AVA](https://ava.li)

Traductions : [English](https://github.com/avajs/eslint-plugin-ava/blob/master/readme.md)


## L'installation

```
$ npm install --save-dev eslint eslint-plugin-ava
```


## L'utilisation

Configurez le dans le `package.json`.

```json
{
	"name": "my-awesome-project",
	"eslintConfig": {
		"env": {
			"es6": true
		},
		"parserOptions": {
			"ecmaVersion": 7,
			"sourceType": "module"
		},
		"plugins": [
			"ava"
		],
		"rules": {
			"ava/assertion-arguments": "error",
			"ava/assertion-message": ["off", "always"],
			"ava/max-asserts": ["off", 5],
			"ava/no-cb-test": "off",
			"ava/no-identical-title": "error",
			"ava/no-ignored-test-files": "error",
			"ava/no-invalid-end": "error",
			"ava/no-only-test": "error",
			"ava/no-skip-assert": "error",
			"ava/no-skip-test": "error",
			"ava/no-statement-after-end": "error",
			"ava/no-todo-test": "warn",
			"ava/no-unknown-modifiers": "error",
			"ava/prefer-power-assert": "off",
			"ava/test-ended": "error",
			"ava/test-title": ["error", "if-multiple"],
			"ava/use-t-well": "error",
			"ava/use-t": "error",
			"ava/use-test": "error",
			"ava/use-true-false": "error"
		}
	}
}
```


## Les règles

Les règles s'activeront uniquement dans les fichiers de test.

- [assertion-arguments](docs/rules/assertion-arguments.md) - Imposer le passage d'arguments corrects aux assertions.
- [assertion-message](docs/rules/assertion-message.md) - Imposer ou interdir les messages d'assertion.
- [max-asserts](docs/rules/max-asserts.md) - Limiter le nombre d'assertions dans un test.
- [no-cb-test](docs/rules/no-cb-test.md) - S'assurer qu'aucun `test.cb()` n'est utilisé.
- [no-identical-title](docs/rules/no-identical-title.md) - S'assurer que chaque test a un titre différent.
- [no-ignored-test-files](docs/rules/no-ignored-test-files.md) - S'assurer qu'aucun test ne soit écrit dans des fichiers ignorés.
- [no-invalid-end](docs/rules/no-invalid-end.md) - S'assurer que `t.end()` est seulement appelé dans `test.cb()`.
- [no-only-test](docs/rules/no-only-test.md) - S'assurer qu'aucun `test.only()` soit présent.
- [no-skip-assert](docs/rules/no-skip-assert.md) - S'assurer qu'aucune assertion soit passée (skip).
- [no-skip-test](docs/rules/no-skip-test.md) - S'assurer qu'aucun test soit passé (skip).
- [no-statement-after-end](docs/rules/no-statement-after-end.md) - S'assurer que `t.end()` soit la dernière instruction exécutée.
- [no-todo-test](docs/rules/no-todo-test.md) - S'assurer qu'aucun `test.todo()` soit utilisé.
- [no-unknown-modifiers](docs/rules/no-unknown-modifiers.md) - Empêcher l'utilisation de modificateurs de test inconnus.
- [prefer-power-assert](docs/rules/prefer-power-assert.md) - Autoriser uniquement l'utilisation des assertions qui n'ont pas d'alternatives dans [power-assert](https://github.com/power-assert-js/power-assert).
- [test-ended](docs/rules/test-ended.md) - S'assurer que les tests de callback soient explicitement terminés.
- [test-title](docs/rules/test-title.md) - S'assurer que les tests ont un titre.
- [use-t-well](docs/rules/use-t-well.md) - Empêcher une mauvaise utilisation de `t`.
- [use-t](docs/rules/use-t.md) - S'assurer que les fonctions de test utilisent `t` comme paramètre.
- [use-test](docs/rules/use-test.md) - S'assurer que AVA est importé avec la variable nommée `test`.
- [use-true-false](docs/rules/use-true-false.md) - S'assurer que `t.true()`/`t.false()` sont utilisés à la place de `t.truthy()`/`t.falsy()`.


## Config recommandée

Ce plugin exporte une [config recommandée](https://github.com/avajs/eslint-plugin-ava/blob/master/index.js) (`recommended`) qui applique les bonnes pratiques.

Activez la dans votre `package.json` avec l'option `extends` :

```json
{
	"name": "my-awesome-project",
	"eslintConfig": {
		"plugins": [
			"ava"
		],
		"extends": "plugin:ava/recommended"
	}
}
```

Consulter les [docs ESLint](http://eslint.org/docs/user-guide/configuring#extending-configuration-files) pour plus d'informations sur l'extension des fichier de config.

**Remarque** : Cette config activera aussi correctement les [options du parser](http://eslint.org/docs/user-guide/configuring#specifying-parser-options) et de l'[environnement](http://eslint.org/docs/user-guide/configuring#specifying-environments).


## Auteurs

- [L'équipe AVA](https://github.com/avajs/ava-docs/blob/master/fr_FR/readme.md#léquipe)
- [Jeroen Engels](https://github.com/jfmengels)
- [Takuto Wada](https://github.com/twada)

[Et nos supers contributeurs](https://github.com/avajs/eslint-plugin-ava/graphs/contributors)


## Licence

MIT © [Sindre Sorhus](https://sindresorhus.com)

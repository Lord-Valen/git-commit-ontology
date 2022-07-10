## Git Commit Ontology

Many [popular git commit message conventions](https://github.com/kazupon/git-commit-message-convention) propose taxonomies of commit message types. Sold on the premise but not quite satisfied with the proposals, this is my attempt to classify different types of commits in a non-arbitrary and relevant way.

Subject to change as my understanding of the nature of software development improves.

## Message Format

>\<emoji> <`type`> \<summary>
>
>[optional details]
>
>[optional footer]

Try not to exceed 50 characters in summary.

Use backticks (\`content\`) around type for special formatting. 

### Example

```
git commit -m ':bulb: `refactor` encapsulate loop execution into own function'
```
> :bulb: `refactor` encapsulate loop execution into own function

## Commit Ontology

| Emoji | Keyword | Meaning | 
| :---- | :------ | :------ |
| :bulb: | `refactor`| Changing the *shape* of code without changing it's *computational space* (rearranging, decoupling, decomposing code)| 
|:brain:| `redesign` | Changing the fundamental approach, architecture, strategy, *computational space* of the program (changing the domain or range of functions, parameterizing encapsulations, switching from static to dynamic design patterns, etc.)|
|:rocket:| `feat` | Adding code that constitutes new features to the program |
|:jigsaw:| `add` | Adding code that does not constitute a feature (encapsulations that have not yet been integrated into an imminent feature, or have been integrated into previous features)|
|:gear:|`value`| Changing arbitrary values in the program (switching out injected dependencies, editing constants/scaling factors, toggling rules/mechanics, etc.)|
|:notes:| `semantic` | Changing types of variables, return types for functions, etc. |
|:bug:| `fix` | Fixing bugs |
|:pencil:| `docs` | Adding/updating documentation|
|:gem:| `style` | Changing characters (whitespace, names, semi-colons, brackets, etc.) |
|:technologist:| `UI` | Changing the user interface (prompts, graphics, audio, client interactions, etc.)|
|:lock:| `access` | Changing visiblity and mutability modifiers (const, private, public, protected, replacing attribute references with getters/setters) |
|:recycle:| `env` | Development environment related changes (tooling, directory structure, filenames) |
|:arrow_up:| `misc` | Any other change |

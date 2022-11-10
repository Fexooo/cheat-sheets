# Deutsches Markdown cheat sheet

Diese Datei erklärt einige basics zu Markdown und ist zum nachgucken der verschiedenen Syntaxe gedacht.

## Headings

Headings sowie Subheadings werden mit der Anzahl an # (Rauten) vor einem Text definiert. Dabei ist es wichtig ein Leerzeichen zwischen Raute und Text zu setzen, andernfalls wird der Text als normaler Text interpretiert.
```mardown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

## Hervorhebungen

Es ist möglich in Markdown Text: **fett**, _kursiv_ oder ~~durchgestrichen~~ anzuzeigen.
Auch ist es möglich diese Arten von Text zu kombinieren: **_~~Beispiel~~_**.
```markdown
**Fett geschriebener Text** kann auch mit __Unterstrichen__ dargestellt werden.

Dasselbe gilt auch für *kursiven* _Text_.

~~Durchgestrichener~~ Text wird mit jeweils 2 Tilden und insgesamt 4 Tilden dargstellt
```

## Zeilenumbrüche

Bei Markdown wird ein Zeilenumbruch nicht einfach mit einem einzelnen Zeilenumbruch in der Quelldatei dargestellt.
```mardown
Dafür sind 2 Zeilenumbrüche in der Quelldatei notwendig.

Ungefähr so!
```

> [!Obsidian]
> In Obsidian werden diese Zeilenumbrüche im Editor automatisch erstellt, daher sind in diesem Editor sind diese doppelten Zeilenumbrüche in dem Editor von Obsidian überflüssig.

## Blockzitat

Es ist möglich Blockzitate darzustellen.
> Das ist ein Blockzitat

```markdown
> Das ist ein Blockzitat
```

## Listen

Listen sind trivial und simple und werden nach ihrer Art definiert.
Die jeweiligen Listen werden wie folgt dargestellt:

### Geordnete Liste

1. Erstes Element
2. Zweites Element
```markdown
1. Erstes Element
2. Zweites Element
```

### Ungeordnete Liste

- Erstes Element
- Zweites Element
```markdown
- Erstes Element
- Zweites Element
```

### Gemischte Liste

Diese beiden Arten sind jeweils kombinierbar.
Auch sind Unterlisten möglich.
Um Unterlisten darzustellen reicht ein Tab.

1. Erstes Element
    - Unterelement
```markdown
1. Erstes Element
	- Unterelement
```


## Links auf externe Webseiten

Links auf externe Webseiten, zum Beispiel [Google](https://www.google.com), werden wie folgt definiert:
```markdown
[Google](https://www.google.com)
```

## Code Blöcke

Um Code Blöcke darzustellen wird der folgende Sytax benutzt:
<pre>
``` [SPRACHE]
Code
```
</pre>

Beispiele:
```javascript
function test() {
	var test = 0
	alert(test)
}
```

```python
def test():
	foo = "Test123"
	print foo
```

## Tabellen

Tabellen Zellen im Header müssen mit mindestens 3 "-" Zeichen separiert.
Die äußeren "pipes" sind optional und werden mit "|" Zeichen dargestellt.

| IDs | Werte | Bemerkungen |
| --- | --- | --- |
| Test | 12 | Keine Bemerkung |
| Test2 | 24 | Test Bemerkung |

Syntax Beispiel:
```markdown
| IDs | Werte | Bemerkungen |
| --- | --- | --- |
| Test | 12 | Keine Bemerkung |
| Test2 | 24 | Test Bemerkung |
```

## HTML Tags

Es ist auch möglich HTML Tags innerhalb Markdown zu verwenden. Um beispielsweise eine horizontale Linie mit dem ```<hr>``` Tag darzustellen.

Beispiel:

<hr>

```html
<hr>
```

# Obsidian

## Besonders hervorgehobene Informationen
> [!Obsidian Informationen besonders hervorheben]
> In Obsidian ist es möglich Informationen auf diese besondere Art darzustellen.

Dafür wird der folgende Syntax verwendet:
```markdown
> [!Obsidian Informationen besonders hervorheben]
> In Obsidian ist es möglich Informationen auf diese besondere Art darzustellen.
```

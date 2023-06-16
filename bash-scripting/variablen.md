# Variablen

## Variable definieren
Eine Variable kann nach folgendem muster definiert werden `variable_name="Wert"`.
Man kan Zahlen oder auch Strings speichern. Hier ein Beispiel:
- `name="Text"`
- `age=20`

Beachte, dass es keine Leerzeichen um das Gleichheitszeichen (=) geben darf.

Variablennamen in Bash können aus Buchstaben, Zahlen und dem Unterstrich bestehen. Sie müssen mit einem Buchstaben oder einem Unterstrich beginnen und dürfen keine Leerzeichen enthalten. Beachte, dass Bash zwischen Groß- und Kleinschreibung unterscheidet. Das bedeutet, dass `name` und `Name` unterschiedliche Variablen sind.

## Variable verwenden
Du kannst auf den Wert einer Variable zugreifen, indem du den Dollarzeichen ($) gefolgt vom Variablennamen verwendest. Ein Beispiel mit dem command echo:

`name="Hans Muster"` <br/>
`age=20` <br/>
`echo $name` <br/>
`echo "Mein Name ist ${name} und ich bin ${age} jahre alt"`
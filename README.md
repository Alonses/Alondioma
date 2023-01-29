<h1>Alondioma</h1>

Esse repositório tem por base reunir todas as traduções e prover linhas de texto para o <a href="https://github.com/Alonses/Alonsal">Alonsal</a>

O Alonsal é configurado para coletar todos os arquivos `.json`, eles são baixados caso tenham alguma alteração
e usados pelo bot em seus comandos.

O Bot ao resgatar uma tradução, também verifica se essa tradução possui outras variantes
de traduções, como no exemplo abaixo:

```
    // Verifica se não há mensagens diferentes para o mesmo retorno
    if (Array.isArray(data))
        phrase = data[Math.floor((data.length - 1) * Math.random())]
```

Caso a tradução tenha sido salva no `json` como um array, com outras frases, como no exemplo abaixo, é escolhida uma
das frases para se retornar ao usuário

```
"saudacoes" : [ "Oi", "Olá", "Opa", "Aoba!"]
```

O mesmo é usado para qualquer idioma, porém, caso determinado idioma não possua a chave, neste caso representada por "saudacoes" no idioma
que o usuário do bot está configurado, é retornado o valor da mesma chave no idioma padrão ( português brasileiro )

<hr/>  <br>

Um caminho até a tradução é definido usando-se os nomes das chaves, por esse motivo, deve-se manter o nome das chaves igual ao arquivo base
( neste caso o pt-br ), para que seu idioma seja compreendido e funcione.

Temos como exemplo de uma chamada de tradução a seguinte linha <br>
`client.tls.phrase(user, "manu.convite.titulo")`
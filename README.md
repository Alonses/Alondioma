#Alondioma

Esse repositório tem por base reunir todas as traduções e prover linhas de texto para o <a href="https://github.com/Alonses/Alonsal">Alonsal</a>

O Alonsal é configurado para coletar todos os arquivos `.json` são baixados caso tenham alguma alteração
e usados pelo bot em seus comandos.

O Bot também ao resgatar uma tradução, também verifica se essa tradução possui outras variantes
de traduções, como no exemplo abaixo:

```
    // Verifica se não há mensagens diferentes para o mesmo retorno
    if (Array.isArray(data))
        phrase = data[Math.floor((data.length - 1) * Math.random())]
```

Caso a tradução tenha sido salva no `json` como um array, com outros modelos, como no exemplo abaixo, é escolhida uma
das frases para se retornar

"saudacoes" : [ "Oi", "Olá", "Opa", "Aoba!"]

O mesmo é usado para qualquer idioma, porém, caso determinado idioma não possua a chave, neste caso chamada de "saudacoes" no idioma
que o usuário do bot está configurado, é retornado o valor da mesma chave no idioma padrão ( português brasileiro )

Veremos como, a partir de uma resposta da requisição, interceptar seu respectivo conteúdo e trabalhar esse conteúdo no front-end da aplicação. Para isso, usaremos o atributo responseText da nossa variável XMLHttpRequest.

é importante acessar esse atributo dentro do readyState, isto porque se colocar após o send, por exemplo, como a requisição é feita de forma assíncrona, depois do send pode ser que ela nao tenha sido carregada imediatamente. Logo, é imporatnte acessá-la quando o state == 4 e status == 200, que quer dizer que a requisição foi carregada.

Caso se confuda, veja o material ../Aula-03/estados_da_requisicao.md

Agora, ao inves de atribuirmos o texto "Requisição finalizada com sucesso", exibiremos o conteúdo recebido como resposta na variavel instanciadora do AJAX.
Requisições assíncronas pt4 - Status da requisição

    https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status
    
    => Respostas de informação (100-199),
    => Respostas de sucesso (200-299),
    => Redirecionamentos (300-399)
    => Erros do cliente (400-499)
    => Erros do servidor (500-599)

    Se você receber uma resposta que não está nesta lista, é uma resposta não padrão, provavelmente personalizada pelo software do servidor.

    200 -> requisição bem sucedida
    404 -> cliente solicitou um recurso que não existe no servidor

    

    -> PARA TER ACESSO AO STATUS DA REQUISIÇÃO FEITA A PARTIR DO CLIENT XMLHttpRequest, basta utilizar o atributo status.

        ajax.status

        supondo que a requisição seja feita solicitando um recurso que não existe, o status retornado será 404
    
        É importante comentar, que diferente do appendChild, o innerHTML substitui todo o conteúdo da tag, ao inves de simplesmente atribuir um novo conteúdo

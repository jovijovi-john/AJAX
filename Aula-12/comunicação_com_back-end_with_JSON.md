Refactoring da comunicação com o back-end utilizando JSON

    notação JSON é nativamente suportado por aplicações web front-end

    APIs:

        RESTfull - Baseada em trocas de dados utilizando JSON
        SOAP - Baseada em trocas de dados utilizando XML

    Baixe o filmes.zip que contém o filmes.
    Ao invés de transformar esse texto transitado na nossa requisição para uma árvore de elementos para depois converter isso para um objeto, nós podemos utilizar a bibliteca JSON e usar o método .parse() para converter essa informação
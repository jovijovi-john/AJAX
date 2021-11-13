Requisições assíncronas pt1 -> Efetuando requisições HTTP via XMLHTTPRequest

    vamos trabalhar apenas com as páginas de conteúdo

    1-> cria o arquivo requisicoes_assincronas.html

     let ajax = new XMLHttpRequest();
    // objeto para configurar url e disparar requisições

    ajax.open('GET', 'pagina_1_conteudo.html')
    // responsável por definir qual url será requisitada, e qual método será utilizado nesse processo

    agora precisamos enviar a requisição (request)
    -> ajax.send()
        console.log(ajax)

    Agora transforma esse código em uma funcao e atribua uma instancia da mesma em cada botão
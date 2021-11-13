Requisições assíncronas pt2 - Estados da requisição (state)

    Atributos que são muito confundidos dentro do objeto XMLHttpRequest:
        -> state: estado
        -> status

    Cada requisição feita a partir do objeto XMLHttpRequest passam por 5 estados diferentes:
    
    o atributo readystate representa o estado do objeto ajax de acordo com a requisição que está sendo feita

    ReadyState:
        0 => request not initialized (requisição não iniciada)
        1 => server connection established (conexão estabelecida com o servidor)
        2 => request received (requisiçãi recebida {pelo servidor})
        3 => processing request (processando requisição)
        4 => request finished and response is ready (requisição finalizada)

        //----------------------------------------------------
        //		Requisição não iniciada, state = 0
        //----------------------------------------------------

        console.log(ajax.readyState)

        
        //----------------------------------------------------------------
        //		Conexão estabelecida com o servidor, state = 1
        //----------------------------------------------------------------

        ajax.open('GET', url)
        console.log(ajax.readyState)

        Os demais estados são notificados pelo servidor para o client. Ou seja, o client precisa estar configurado para ficar ouvindo esses eventos do servidor. Logo, quem starta o progresso do estado da requisição não é mais o client, mas sim a aplicação servidora

        Para ficar ouvindo essa mudança de estado, utilizamos o método send.

        O atributo onreadystatechange => disparado sempre que o estado do objeto AJAX é modificado. Inclusive quando essa mudança é proviniente do servidor.
            -> geralmente esse atributo recebe uma função, ai acaba se tornando um método.
            Sempre quando existe uma mudança  de estado e essa mudança está completa, nós executamos alguma coisa.

        Na prática, usamos majoritariamente o estado 4 (requisição finalizada). Não significa que foi finalizada com a resposta desejada

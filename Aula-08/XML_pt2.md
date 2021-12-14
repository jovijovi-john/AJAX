Recuperando arquivo XML do servidor via HTTP

    Vamos fazer uma página web que apresente uma relaçõ de filmes. Essa relação de filmes será incluida nessa página através de uma requisição de um arquivo XML que esteja disponível no servidor.

    A ideia é trazer para o browser do cliente, através de uma requisição HTTP a página filmes.html. Quando essa página estiver renderizada, através do XMLHttpRequest requisitar o arquivo filmes.xml, que contém a relação de filmes. Ao receber essa resposta, manipularemos o DOM inserindo cada um desses filmes nessa página.

    Esse arquivo XML contém apenas os dados que essa aplicação precisa exibir.

    primeira coisa que devemos fazer é baixar o arquivo da aula (filmes.zip)
    Dentro dele teremos o filme.xml, cujo qual é composto por uma relação de filmes.
    Cada filme tem título, resumo, 1 ou vários generos, com 1 ou mais atores. 

    A versão é obrigatória mas o encoding é opcional
    Link da estrutura XML: https://www.w3schools.com/xml/xml_tree.asp
    
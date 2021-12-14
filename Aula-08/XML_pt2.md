Recuperando arquivo XML do servidor via HTTP

    Vamos fazer uma página web que apresente uma relaçõ de filmes. Essa relação de filmes será incluida nessa página através de uma requisição de um arquivo XML que esteja disponível no servidor.

    A ideia é trazer para o browser do cliente, através de uma requisição HTTP a página filmes.html. Quando essa página estiver renderizada, através do XMLHttpRequest requisitar o arquivo filmes.xml, que contém a relação de filmes. Ao receber essa resposta, manipularemos o DOM inserindo cada um desses filmes nessa página.

    Esse arquivo XML contém apenas os dados que essa aplicação precisa exibir.
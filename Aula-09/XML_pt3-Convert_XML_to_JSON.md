XML parte 3 - Convertendo o XML para JSON e o porquê.

    Por quê?
        O XML não é suportado nativamente pelo JAVASCRIPT, diferentemente do JSON. Além disso, a requisição que estamos fazendo retorna uma string, e os dados que são trafegados entre client e server são basicamente textos. Por isso que esses textos precisam de marcações, para que associados a esses textos seja possível incluir metadados.

        O JSON também trafega em formato texto, não temos objetos sendo trafegados em requisições HTTP, são puramente textos. O JSON, diferentemente do XML, é nativamente suportado pelo JS.

        Baixe o xmltojson.zip
        Inclua o script no filmes.html

        Precisamos converter esse texto puro em uma árvore de elementos, semelhante ao DOM. Para isso utilizaremos a Class DOMParser
        let parser = new DOMParser();
        
        xmlFilmes = parser.parserFromString(String que eu quero fazer o parser, notação utilizada para composição dessa string);

        ex:

              domFilmes = parser.parserFromString(XMLFilmes, "text/xml")
              domFilmes = parser.parserFromString(XMLFilmes, "text/json")
              domFilmes = parser.parserFromString(XMLFilmes, "text/html")

        Agora, de posse de uma árvore de elementos, podemos utilizar o JS para convertê-la para um objeto JSON.
        a função xmlToJson retorna um objeto:
            
            let jsonFilmes = xmlToJson(domFilmes);
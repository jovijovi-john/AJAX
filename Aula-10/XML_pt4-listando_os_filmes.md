Vamos manipular o objeto json de modo a recuperar a relação de filmes e listá-la na nossa página. Utilizaremos um laço de repetição para este fim.

Nessa aula adicionaremos elementos html estáticos mas depois faremos um refactoring desses elementos os utilizando de maneira dinâmica

importante comentar o seguinte:

    let divRow = document.createElement("div")
    let divCol = document.createElement("div")

    ...

    divRow.appendChild(divCol)
    
    divCol.appendChild(p1)
    divCol.appendChild(p2)
    divCol.appendChild(hr)
    
    let container = document.getElementById("lista")
    container.appendChild(divRow)

mesmo que eu tenha adicionado divCol à divRow antes de eu atribuir p1, p2, hr... à divCol, ainda assim vai dar certo, pois aparentemente o JS adiciona por referência, então mesmo que eu adicione um bilhao de coisas depois em divCol, essas coisas ainda estarão presentes de forma atualizada na divRow.

Outra coisa importante:
    
    não faça:
        let elemento = createElement("div").innerHTML = "<p>oi</p>"
    
    isso não funciona

    faça:
        let elemento = createElement("div")
        elemento.innerHTML = "<p>oi</p>"
# useState

<figure><img src=".gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Se trata de uma hook que facilita o manuseio do estado dos componentes. O estado se refere aos dados manipulados pelo componente, os dados que esse componente recebe.&#x20;

ps: usamos os state pois criamos as consts setState, que pode ser manipulada e os valor alterado.&#x20;

No exemplo abaixo temos um formulário com dois inputs, name e password

````javascriptreact
```javascriptreact
import { useState } from "react"

function Form() {

function cadastrarUsuario(e){
    e.preventDefault()
    console.log(name)
    console.log("cadastrado")
}

const [name, setName] = useState()

    return(
        <div>
            <h1>Meu cadastro:</h1>
            <form onSubmit={cadastrarUsuario}>
                <div>
                    <label htmlFor="nome">Nome:</label>
                    <input 
                    type="text" 
                    id="name" 
                    name="name" 
                    placeholder="Digite o seu nome" 
                    onChange = {(e) => setName(e.target.value)}/>
                    
                </div>
                <div>
                    <label htmlFor="password">Senha:</label>
                    <input 
                    type="password" 
                    id="password" 
                    name="password" 
                    placeholder="Digite a sua senha" />
                </div>
                <div>
                    <input type="submit" value="Cadastrar" />
                </div>
            </form>
        
        </div>
    )

}

export default Form
```
````

Neste exemplo nós importamos o useState ![](<.gitbook/assets/image (5) (1) (1).png>)

Criamos uma const ![](<.gitbook/assets/image (6).png>)

E adicionamos  ao input a seguinte açao: a cada vez que a variavel name mudasse, o useState atualizaria a variavel setName ![](<.gitbook/assets/image (8).png>)



Se fosse um caso de ediçao de form, o nome já viria setado e o value name![](<.gitbook/assets/image (9).png>)

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

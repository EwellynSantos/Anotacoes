# Modificadores de acesso

## Modificadores para Membros

Os membros de uma classe podem ser atributos, métodos, propriedades e etc.

<table><thead><tr><th width="128">Modificador</th><th width="99" align="center">Mesma classe</th><th width="112" align="center">Classe filha</th><th width="109" align="center">Mesmo projeto</th><th width="120" align="center">Outro projeto</th></tr></thead><tbody><tr><td><code>public</code></td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td><code>private</code></td><td align="center">✅</td><td align="center">❌</td><td align="center">❌</td><td align="center">❌</td></tr><tr><td><code>protected</code></td><td align="center">✅</td><td align="center">✅</td><td align="center">Apenas se herdar</td><td align="center">Apenas se herdar</td></tr><tr><td><code>internal</code></td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center">❌</td></tr><tr><td><code>protected internal</code></td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center">Apenas se herdar</td></tr><tr><td><code>private protected</code></td><td align="center">✅</td><td align="center">✅</td><td align="center">Apenas se herdar</td><td align="center">❌</td></tr></tbody></table>

***

## Modificadores de Classes

**Classes top-level**

É permitido **apenas** o uso de  `public` e `internal`.  Al\[em disso, caso nao adicione um modificador de acesso a classe, por padrão ela será internal.&#x20;

Nesse caso, **NÃO** pode fazer:

```csharp
namespace MeuProjeto
{    
    private class Pessoa // ❌ Erro de compilação    
    {    
    }
}
```

**Classes nested class**

Classes aninhadas, ou seja, que estão dentro da classe top-level, podem usar **todos** os modificadores de acessos.

Em resumo:

✔️ **Classe de nível superior:**

```csharp
public class Pessoa { }   // ✔
internal class Pessoa { } // ✔
class Pessoa { }          // ✔ (internal)
private class Pessoa { }  // ❌ -> não pode
protected class Pessoa { }// ❌ -> não pode
```

✔️ **Classe aninhada:**

```csharp
public class Empresa
{    
    private class Funcionario { }          // ✔    
    protected class Departamento { }       // ✔    
    internal class Setor { }               // ✔    
    public class Cliente { }               // ✔    
    protected internal class Gerente { }   // ✔    
    private protected class Diretor { }    // ✔
}
```

***

### Ordem sugerida para a estrutura de uma classe ![](<.gitbook/assets/image (3).png>)

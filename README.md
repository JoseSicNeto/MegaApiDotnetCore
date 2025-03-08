# **Megaman API**

![Capacete do robô](https://github.com/Paulomarvel/MegaApiDotnetCore/blob/master/_docs/Astrobot%20avatar.png)

## 📖 **Descrição do Projeto**
A **Megaman API** é uma aplicação desenvolvida em **.NET Core 3.1** que oferece uma interface para acessar informações detalhadas sobre os chefes do jogo *Megaman*. A API retorna dados no formato JSON, facilitando sua integração com outros sistemas e aplicações.

Exemplo de resposta JSON fornecida pela API:
```json
{
  "Id": 1,
  "Code": "DLN/DRN-003",
  "Name": "Cutman",
  "HP": 150,
  "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
}
```

📖 [Documentação Detalhada](https://github.com/Paulomarvel/MegaApiDotnetCore/blob/master/_docs/Megaman_API_Documentacao.pdf)

---

## 🚀 **Tecnologias Utilizadas**
| Tecnologia                     | Versão  | Descrição                                           |
|---------------------------------|---------|---------------------------------------------------|
| **.NET Core**                  | 3.1     | Framework para criação de APIs RESTful            |
| **Entity Framework Core**      | 3.1.8   | ORM para manipulação de banco de dados            |
| **SQL Server**                 | N/A     | Banco de dados utilizado                          |
| **Newtonsoft.Json**            | 12.0.2  | Biblioteca para manipulação de JSON               |

---

## 📦 **Dependências**
| Dependência                     | Versão  | Link                                              |
|---------------------------------|---------|--------------------------------------------------|
| Microsoft.EntityFrameworkCore   | 3.1.8   | [EntityFrameworkCore](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/) |
| Microsoft.EntityFrameworkCore.Design | 3.1.8 | [EntityFrameworkCore.Design](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/) |
| Microsoft.EntityFrameworkCore.SqlServer | 3.1.8 | [EntityFrameworkCore.SqlServer](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/) |
| Newtonsoft.Json                 | 12.0.2  | [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/) |

---

## 📂 **Estrutura do Projeto**
```plaintext
.vs/
.vscode/
bin/
Controllers/
    RobotsController.cs
Database/
middlewares/
Models/
obj/
Properties/
Services/
appsettings.Development.json
appsettings.json
global.json
MegamanApi.csproj
MegamanApi.sln
Program.cs
Startup.cs
```

### 📁 **Descrição das Pastas**
| Pasta              | Descrição                                                |
|---------------------|--------------------------------------------------------|
| **Controllers/**    | Contém os controladores que definem os endpoints da API |
| **Database/**       | Gerencia conexões e mapeamentos com o banco de dados    |
| **middlewares/**    | Implementação de middlewares                            |
| **Models/**         | Define as classes e modelos de dados                    |
| **Services/**       | Contém lógica de negócio e serviços usados pelos controladores |
| **appsettings.json**| Configurações gerais do projeto                         |
| **Startup.cs**      | Configuração inicial dos serviços e pipeline HTTP       |

---

## 🌐 **Endpoints**
### 🔍 **GET** `/api/v1/robots`
Retorna todos os robôs cadastrados.
**Exemplo de Resposta:**
```json
[
  {
    "Id": 1,
    "Code": "DLN/DRN-003",
    "Name": "Cutman",
    "HP": 150,
    "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
  }
]
```

---

### 🔍 **GET** `/api/v1/robots/{id}`
Retorna detalhes de um robô específico pelo ID.
**Exemplo de Resposta de Sucesso:**
```json
{
  "Id": 1,
  "Code": "DLN/DRN-003",
  "Name": "Cutman",
  "HP": 150,
  "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
}
```
**Exemplo de Resposta de Erro:**
```json
{
  "message": "Nenhum robo encontrado"
}
```

---

### ➕ **POST** `/api/v1/robots`
Adiciona um novo robô ao sistema.
**Exemplo de Resposta de Sucesso:**
```json
{
  "message": "Robô criado com sucesso"
}
```

---

## 🔧 **Configuração e Execução**
1. **Clone o Repositório**
   ```bash
   git clone https://github.com/seu-usuario/MegamanApi.git
   cd megaman-api
   ```

2. **Instale as Dependências**
   Certifique-se de ter o SDK .NET Core 3.1 instalado.
   ```bash
   dotnet restore
   ```

3. **Configure o Banco de Dados**
   Atualize o arquivo `appsettings.Development.json` com as credenciais do banco.

4. **Execute o Projeto**
   ```bash
   dotnet run
   ```

5. **Acesse a API**
   A API estará disponível em `http://localhost:5000/api/v1/robots`

---

## 📝 **Considerações Finais**
A API foi desenvolvida seguindo boas práticas de arquitetura em camadas e organização modular para facilitar o entendimento, a manutenção e a extensão do projeto. Contribuições são bem-vindas!

---

## ⚙️ **Licença**
Este projeto está licenciado sob a [MIT License](https://opensource.org/licenses/MIT). Fique à vontade para usá-lo e adaptá-lo às suas necessidades.

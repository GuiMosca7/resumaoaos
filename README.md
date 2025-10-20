# resumaoaos
EXERCÍCIO 1 
Explique brevemente a função de cada camada em uma arquitetura orientada a serviços:
a) Camada de Apresentação (Controller):

RECEBE REQUISIÇOES DO FRONT

b) Camada de Serviço (Service):

define as regras de negocios, parte q a logica vai funcionar

c) Camada de Repositório (Repository):

faz a conexao entre o model e o bd

d) Camada de Modelo (Entity/Domain):

onde definimos as classes, getters e setters para encapsulamento, sobreescrevemos metodos, etc

EXERCÍCIO 2 
Analise as afirmativas sobre arquitetura em camadas:
( f) A camada de apresentação deve conter regras de negócio complexas
( f ) É uma boa prática que a camada de serviço acesse diretamente o banco de dados
( v ) A camada de repositório deve ser responsável apenas pelo acesso a dados
( f) O controller deve chamar diretamente métodos do repositório
( v ) A camada de serviço orquestra a lógica de negócio da aplicação

EXERCÍCIO 3
Liste 5 boas práticas para documentação de APIs utilizando OpenAPI/Swagger:
1. endpoints 
2. Descreva a autenticação.
3. Valide a sua especificação.
4. inclua anotações de código
5. esquema de erro padronizado.


EXERCÍCIO 4 
Defina os seguintes conceitos e dê um exemplo prático de cada:
a) Coesão:
   Definição: um modulo tem o nome de acordo com as suas funcoes
   Exemplo: calculadora tem metodos para calcular

b) Acoplamento: 
   Definição: grau de dependencia entre modulos
   Exemplo: O Módulo B conhece todos os detalhes de como o Módulo A calcula o preço.
Se a lógica do Módulo A mudar, o Módulo B também precisa ser alterado.

c) Encapsulamento:
   Definição: atributos privados de uma classe
   Exemplo: a classe conta tem o saldo privado

d) Abstração:
   Definição: princípio de esconder os detalhes internos de funcionamento de um sistema ou objeto e mostrar apenas o que é necessário para quem o utiliza.
   Exemplo: Você aperta o botão → a luz acende ou apaga.

Você não precisa saber:

Como a eletricidade funciona
Como os fios estão ligados
Como a lâmpada acende


EXERCÍCIO 5 
Reescreva o código abaixo utilizando Optional para evitar NullPointerException:

import java.util.Optional;

public String buscarNomeUsuario(Long id) {
    Optional<Usuario> optionalUsuario = usuarioRepository.findById(id);

    return optionalUsuario.map(Usuario::getNome)
                           .orElse("Usuário não encontrado");
}


EXERCÍCIO 6 - JPA E GERAÇÃO DE IDs
a) Explique o que é GenerationType.IDENTITY:
gerador de chave primaria
b) Cite 2 limitações desta estratégia em cenários de alta concorrência:
1. gerar chaves sem limites definidos
2. sobrecarga de banco

c) Qual alternativa você sugeriria para resolver essas limitações?
1- gerar id de forma diferente com verificao
2- fazer verificaçao de forma diferente


 	 

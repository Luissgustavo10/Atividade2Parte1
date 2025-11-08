# Atividade2Parte1

1)JSON (JavaScript Object Notation) é um formato leve de troca de dados baseado em texto.
Ele é utilizado para representar objetos e arrays de forma estruturada, usando a sintaxe do JavaScript, mas pode ser lido e gerado por praticamente qualquer linguagem de programação.
Exemplo de JSON:
{
  "nome": "Ana",
  "idade": 25,
  "ativo": true
}

2) Diferença entre JSON.stringify() e JSON.parse()
3) Exemplo
JSON.stringify()	Converte um objeto JavaScript em uma string JSON	JSON.stringify({nome: "Ana"}) → '{"nome":"Ana"}'
JSON.parse()	Converte uma string JSON em um objeto JavaScript	JSON.parse('{"nome":"Ana"}') → {nome: "Ana"}

Exemplo prático:

// Objeto JavaScript
const pessoa = { nome: "João", idade: 30 };

// Enviando dados para um servidor (precisa ser string)
const json = JSON.stringify(pessoa);
console.log(json); // '{"nome":"João","idade":30}'

// Recebendo dados do servidor (vem como string)
const obj = JSON.parse(json);
console.log(obj.nome); // "João"

3. Manipulação da string "JavaScript é baseada em ECMA Script"

const texto = "JavaScript é baseada em ECMA Script";

// a) Verificar se contém a palavra "Script"
console.log(texto.includes("Script")); // true

// b) Remover a palavra "JavaScript" e gerar uma nova string
const semJavaScript = texto.replace("JavaScript", "");
console.log(semJavaScript.trim()); // "é baseada em ECMA Script"

// c) Substituir "baseada" por "tem origem"
const substituido = texto.replace("baseada", "tem origem");
console.log(substituido); // "JavaScript é tem origem em ECMA Script"

4. Vantagem de usar template strings (``) em vez de concatenação com +

As template strings (ou template literals) permitem:

Inserir variáveis e expressões diretamente dentro da string usando ${ };

Quebras de linha e formatação mais legível sem precisar de + ou \n.


Exemplo com concatenação tradicional:

const nome = "Ana";
const idade = 25;
const mensagem = "Olá, meu nome é " + nome + " e tenho " + idade + " anos.";

Exemplo com template string:

const mensagem = `Olá, meu nome é ${nome} e tenho ${idade} anos.`;

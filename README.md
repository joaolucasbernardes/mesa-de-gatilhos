# Mesa de Gatilhos

Painel para gerenciar sensores virtuais de uma skill própria de Smart Home
da Alexa, hospedada na AWS a partir do projeto
[sweharris/Alexa-Smart-Home-VirtualButtons](https://github.com/sweharris/Alexa-Smart-Home-VirtualButtons).

Os sensores servem de gatilho para rotinas da Alexa, o que permite acionar
essas rotinas por uma chamada HTTP, vinda por exemplo de um atalho do
iPhone.

## O que a página faz

- Lista os gatilhos cadastrados e o estado de cada um.
- Cria, renomeia e apaga gatilhos.
- Dispara um gatilho para testar a rotina ligada a ele.
- Monta o corpo da requisição pronto para colar no app Atalhos.

## O que a página não contém

Nenhum endereço de API, nenhuma senha, nenhum identificador de conta.

Quem abre a página encontra campos vazios. O endereço da API e a senha são
digitados por quem usa e ficam guardados apenas no `localStorage` daquele
navegador. Eles nunca são enviados para lugar nenhum além da própria API
de quem digitou.

## Para usar

Abra a página, preencha o endereço da sua API e a senha, e clique em
Conectar.

A API precisa liberar chamadas de navegador vindas da origem onde esta
página está hospedada. Em uma HTTP API do API Gateway isso é a configuração
de CORS, permitindo o método `POST` e os cabeçalhos `content-type` e
`authorization`.

## Licença

Mesma licença do projeto original.

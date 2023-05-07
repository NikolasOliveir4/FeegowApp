# FeegowApp

Projeto realizado para teste full-stack da Feegow

---

## Intuito da aplicação

Pensando em um sistema de gestão onde usuários necessitem cadastrar Clientes  

## Como clonar o projeto?

No seu terminal, clone o projeto com o comando abaixo:

```bash
git clone https://github.com/NikolasOliveir4/FeegowApp.git
```
---

# Frontend

O frontend do projeto foi feito em VueJS (utilizando vue-cli).
Nele foram utilizados:

- [Sweetalert](https://sweetalert2.github.io/) (Para as notificações internas)
- [Vue-the-mask](https://www.npmjs.com/package/vue-the-mask) (Para adicionar máscaras aos campos necessários dentro do sistema)
- [Node](https://nodejs.org/en/download/)

## Como rodar?

### Para ambiente de desenvolvimento:

```bash
cd <pasta-do-frontend>
npm run serve
```

_Após o comando terminar, o projeto estará rodando na porta 8080 (http://localhost:8080)_

---
## Como utilizar o sistema?

Ao acessar a url  _http://localhost:8080_ será redirecionado para a página principal e única
Onde terá a listagem dos funcionários, clique no botão Vacinas. 
A listagem irá alterar para a listagem de vacinas, adicione uma vacina primeiramente, clicando no botão `+Nova Vacina`.
Após adicionar uma vacina poderá voltar para o cadastro de Funcionários. 
Clique em `+Novo Funcionário`, a vacina que você cadastrou agora estará na listagem das vacinas.


---
## Algumas regras de negócio?

Visando que os funcionários e aas vacinas sejam dados sensíveis, o sitema foi desenvolvido pensado na não exclusão de dados.
Os dados são apenas inativados, assim podendo manter um histórico em casos de possíveis relatórios a serem gerados futuramente.
Se a Data de validade da Vacina vencer, a mesma irá ser automaticamente inativada e assim saindo das listagens.
Se um funcionário e/ou vacina for deletado(a), será inativado.
Nomes pequenos são verificados antes de serem salvos.
Há validações de CPF/CNPJ e email.
Não é possível uma data de nascimento posterior ao dia atual.


---
## Informações adicionais:

O sistema tem a possibilidade de cadastrar CNPJ visando possíveis pessoas jurídicas que prefiram utilizar CNPJ.
Quanto a questão do sistema não deletar dados e apenas inativar, a alteração seria bem simples.

Atualmente a verificação da validade das vacinas é feito junto da função de listagem, causando um gasto desnecessário de processamento, em caso do sistema ficar hospedado em um servidor, seria substituido por CRON que rodaria um script 1x ao dia.

O repositório se encontra privado no momento devido ao processo seletivo ainda estar acontecendo.

---

Imagens e paleta de cores retiradas do site da [Feegow](https://feegowclinic.com.br/)

Teste feito por Níkolas Oliveira.

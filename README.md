

# Projeto de seleção Coopersystem  
  
O teste consiste em criar uma mini aplicação que simula um resgate personalizado de fundos de investimentos em ações.  
  
Estamos buscando perfis tanto para web quando para mobile, fique a vontade  
para realizar os testes nos 2 ambientes, ou somente oque no que se sentir mais confortável.  
  
Serão avaliados:  
* Integração com api rest!  
* Navegação entre telas  
* Validação de formulários conforme regras de negócios  
* Padrões de codificação  
* Teste unitários  
	* Angular JS (karma/jasmine)  
	* React native ( jest js )  
  
Obs: Os layouts dos protótipos são só ilustrativos, fiquem a vontade  
para fazer suas modificações.  
  
### Protótipos  
* React Native  
	* [Lista de investimentos](https://raw.githubusercontent.com/Leonardo270593/avaliacao-coopersystem/master/prototipos-react-native/1%20-%20Lista%20de%20investimentos.png)  
	* [Resgate personalizado](https://raw.githubusercontent.com/Leonardo270593/avaliacao-coopersystem/master/prototipos-react-native/2%20-%20Simula%C3%A7%C3%A3o%20do%20resgate.png)  
	* [Modal de confirmação](https://raw.githubusercontent.com/Leonardo270593/avaliacao-coopersystem/master/prototipos-react-native/3%20-%20Confirma%C3%A7%C3%A3o.png)
  
  
* Angular JS  
	* [Lista de investimentos](https://raw.githubusercontent.com/leonardo-coopersystem/avaliacao-coopersystem/master/prototipos-angularJS/1%20-%20Lista%20de%20investimentos.png)  
	* [Resgate personalizado](https://raw.githubusercontent.com/leonardo-coopersystem/avaliacao-coopersystem/master/prototipos-angularJS/2%20-%20Simula%C3%A7%C3%A3o%20do%20resgate.png)  
	* [Modal de confirmação](https://raw.githubusercontent.com/leonardo-coopersystem/avaliacao-coopersystem/master/prototipos-angularJS/3%20-%20Confirma%C3%A7%C3%A3o.png)
  
### Fluxo de navegação  
* Lista de investimentos  
	* Executar uma chamada get no endereço [http://www.mocky.io/v2/5e76797e2f0000f057986099](http://www.mocky.io/v2/5e76797e2f0000f057986099)
	* Montar a  tela conforme o protótipo fazendo a integração com a resposta da execução do serviço acima.
	* Ao clicar em um plano que  não esta em carência (indicadorCarencia = 'N'), navegar para próxima tela. 
*  Resgate personalizado  
	 * Montar a  tela conforme o protótipo usando as informações do investimento selecionado na tela anterior.
	 * Digitar os valores que deseja resgatar de cada ação e clicar em confirmar resgate
* Modal de confirmação
	* Montar a  tela conforme o protótipo.

### Regras de Negocio  
* Lista de investimentos  
	* Fundos de investimentos em carência (indicadorCarencia = 'S') não pode realizar resgate, deve ficar desabilitado na lista de investimentos.  
  
* Resgate personalizado  
	* Valor a resgatar de cada ação não pode ser maior que saldo acumulado da mesma, deve ser exibido um alerta para cliente quando isso acontecer.  
	* A cada interação, deve ser atualizado o valor total a resgatar.  
	* Valor total a resgatar não pode ser maior que valor total disponível, deve ser exibido um alerta para cliente quando isso acontecer.  
	* Ao clicar no botão de confirmar, alem de validar as regras acimas, deve validar se o valor total a resgatar e maior que 0, caso o contrario, deve exibir um alerta ao cliente para preencher os valores a resgatar da forma que ele deseja.  
	* Ao clicar no botão cancelar, deve voltar pra tela de lista de investimentos.  
	* Após todas a validações deve abrir o modal de confirmação.

### Entrega
Enviar link do github com os testes para o email
leonardo.guedes@coopersystem.com.br

### Telefone para duvidas
61 9 8193-1274

### JSON

Caso o link do json não estiver disponível, pode usar este site para criar um novo endpoint

[https://www.mocky.io/](https://www.mocky.io/)

    {
	  "response": {
	    "status": "200",
	    "data": {
	      "listaInvestimentos": [
	        {
	          "nome": "INVESTIMENTO I",
	          "objetivo": "Minha aposentadoria",
	          "saldoTotalDisponivel": 39321.29,
	          "indicadorCarencia": "N",
	          "acoes": [
	            {
	              "id": "1",
	              "nome": "BBAS3",
	              "percentual": 28.1
	            },
	            {
	              "id": "2",
	              "nome": "VALE3",
	              "percentual": 20.71
	            },
	            {
	              "id": "3",
	              "nome": "PETR4",
	              "percentual": 21.63
	            },
	            {
	              "id": "4",
	              "nome": "CMIG3",
	              "percentual": 12.41
	            },
	            {
	              "id": "5",
	              "nome": "OIBR3",
	              "percentual": 17.15
	            }
	          ]
	        },
	        {
	          "nome": "INVESTIMENTO II",
	          "objetivo": "Viajem dos sonhos",
	          "saldoTotalDisponivel": 7300,
	          "indicadorCarencia": "N",
	          "acoes": [
	            {
	              "id": "1",
	              "nome": "BBAS3",
	              "percentual": 35.81
	            },
	            {
	              "id": "2",
	              "nome": "VALE3",
	              "percentual": 26.42
	            },
	            {
	              "id": "3",
	              "nome": "PETR4",
	              "percentual": 37.77
	            }
	          ]
	        },
	        {
	          "nome": "INVESTIMENTO III",
	          "objetivo": "Abrir meu próprio negócio",
	          "saldoTotalDisponivel": 26000,
	          "indicadorCarencia": "N",
	          "acoes": [
	            {
	              "id": "1",
	              "nome": "BBAS3",
	              "percentual": 41.1
	            },
	            {
	              "id": "2",
	              "nome": "VALE3",
	              "percentual": 22.43
	            },
	            {
	              "id": "3",
	              "nome": "PETR4",
	              "percentual": 26.12
	            },
	            {
	              "id": "5",
	              "nome": "OIBR3",
	              "percentual": 10.35
	            }
	          ]
	        },
	        {
	          "nome": "INVESTIMENTO IV",
	          "objetivo": "Investimento em carencia",
	          "saldoTotalDisponivel": 44000,
	          "indicadorCarencia": "S",
	          "acoes": [
	            {
	              "id": "1",
	              "nome": "BBAS3",
	              "percentual": 41.1
	            },
	            {
	              "id": "2",
	              "nome": "VALE3",
	              "percentual": 22.43
	            },
	            {
	              "id": "3",
	              "nome": "PETR4",
	              "percentual": 26.12
	            },
	            {
	              "id": "5",
	              "nome": "OIBR3",
	              "percentual": 10.35
	            }
	          ]
	        }
	      ]
	    }
	  }
	}

### BOA SORTE! =)

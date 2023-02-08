# Aprendendo a testar
Escopo e subprodutos de teste para o site: [http://www.aprendendotestar.com.br/treinar-automacao.php](http://www.aprendendotestar.com.br/treinar-automacao.php)

Para esse projeto o Documento que traz a abordagem completa utilizada é o: [Plano de teste do projeto!] e pode ser beixado para melhor vizualização.
Este documento traz como aspectos mais importantes as seguintes abordagens sobre o site:


* Casos de teste. 
* Ferramentas de teste. 
* Modelos de teste. 
* Resultados de teste. 
* Subprodutos de teste. 
* Cobertura de teste. 

## Casos de teste

* Enviar Registro
* Atualizar
* Consultar banco
* Apagar


## Ferramentas

Para esse projeto os testes foram realizados em uma máquina local Linux Ubuntu 22.04.1 LTS com acesso à internet e o aplicativo de captura de tela, utilizado o navegador firefox 109.0 (64-bits), e a ferramenta de captura de interações Katalon Recorder 5.5.3.

## Modelos

Não vou colocar todos os modelos aqui pois eles são muitos e podem ser vistos no [Plano de teste do projeto!]
Porém, seguem alguns dos exemplos realizados:


| Númeração | Cenário | Localização | Pré-condição | Procedimento | Resultado esperado:
| ------------- |:-------------:| -----:| ------------- |:-------------:| -----:|
| 1 | Registro | Tela Principal | Nome,usuário e senha válidos | Preencher: - nome - usuário - senha - confirmação de senha|Usuário criado com sucesso!. |
|2  | Registrar duplicado, inválido| Tela Principal | Nome, usuário e senha pré-cadastrados. | Preencher: - nome - usuário - senha. <br/> Clicar: -enviar | Indicar o erro do usuário(registro já existente) e não cadastrar. |
|3 | Registra, em branco, inválido | Tela Principal | Sem pré condição | Clicar: -enviar | Indicar o erro do usuário(campo em branco) e não cadastrar. |
|4 | Registro, poucos caracteres, inválido | Tela Principal | Nome,usuário e senha com menos de 3 caracteres | Preencher: - nome - usuário - senha. <br/> Clicar: -enviar | Indicar o erro do usuário(poucos caracteres) e não cadastrar. |
|5 | Registro, muitos caracteres, inválido | Tela Principal | Nome,usuário e senha com mais de 10 caracteres | Preencher: - nome - usuário - senha  <br/> Clicar: -enviar | Indicar o erro do usuário(excedeu caracteres) e não cadastrar. |


## Resultados

Não vou colocar todos os resultados aqui pois eles são muitos e podem ser vistos no [Plano de teste do projeto!]
Porém, seguem alguns dos exemplos obtidos:


|Númeração|Resultado <br/> Esperado\|Obtido|  Sucesso  |Considerações|
| ------------- |:----------------:|:--------:| ------------- |
|6|Indicar o erro do usuário(caractere inválido) e não cadastrar. <br/> \| <br/> Usuário criado com sucesso!|Falha ❌|
|7|Atualiza e carrega de novo a página. <br/> \| <br/> Atualiza e carrega de novo a página. | Sucesso ✅|
|8|Deleta o registro selecionado. <br/> \| <br/> Deleta o registro selecionado |Sucesso ✅|


## Subprodutos
Os subprodutos tais como: scripts, imagens e vídeos resultados dos testes executados estão disponíveis neste repositório em suas respectivas pastas.
#### Imagens e vídeos relacionados aos casos de teste descritos neste documento possuem a numeração relacionada!


### Algumas gravações dos testes Manuais realizados:


[registro com poucos caracteres nos campos de texto](https://user-images.githubusercontent.com/34687381/217560734-112be533-5d8f-406d-9d9d-e149dda3d3d5.webm)


[registro com campos em branco!](https://user-images.githubusercontent.com/34687381/217560563-8363b1fe-adec-4d1b-8751-fbd0d1883083.webm)


## Cobertura

O nível de cobertura de testes é medido pela “%” porcentagem dos casos de teste executados com sucesso.

|Aceitação Completa |Acima de 95% dos casos de teste executados com sucesso!|O programa está pronto para o deploy!|
| ------------- |:----------------:|:--------:|
|Meio nível de aceitação|De 70 até 95% dos casos executados com sucesso|O programa pode ser liberado para o PO como um protótipo.|
|Inaceitável|Até 70% de casos executados com sucesso.|Qualidade insuficiente.|

##### O projeto atual se encontra com 50% dos seus testes executados com sucesso, o que o coloca em inaceitável!


<br/> 

[//]: <> (Links)

[Plano de teste do projeto!]: https://github.com/lucas-dejard/Site-analise-2/blob/main/site%202%20-%20TestPlan.docx

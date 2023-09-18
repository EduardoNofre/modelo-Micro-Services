## Support & Feedback<BR>
Este projeto é mantido por Eduardo Nofre. Por favor, entenda que não poderemos fornecer suporte individual por e-mail. Acredito também que a ajuda é muito mais valiosa se for partilhada publicamente, para que mais pessoas possam beneficiar dela.

## modelo-Micro-Services<BR>

Modelo de micro services para uso no dia  a dia.
Tem como objetivo servi como um modelo de construção de micro serviço Java. Um padrão a ser seguido.

<p align="center">
   <a href="#requisitos-para-o-desenvolvimento-backend">Requisitos Backend</a> •
   <a href="#ide-eclipse">Ide Eclipse</a> •
   <a href="#configurar-sonar-no-eclipse">Sonar</a> •
   <a href="#configurar-jacoco">Jacoco</a> •
   <a href="#plugin-sonarlint">sonarlint</a> 
</p>

## `Requisitos para o desenvolvimento Backend`
- Eclipse STS 4.19
- JAVA 11 
- Plugin SonarLint
- Spring boot 
- Spring Cloud OpenFeign
- JPA
- Swagger 
- ModelMapper 
- jacoco 
- Lombok

  <h1 align="center">
       Configurações do eclipse para o projeto
   </h1>
   
### 'Configurar sonar no eclipse'
#### Passo 1:<br>
   • Vá ate o seu projeto e clique bom o botão direito sobre ele. Será exibidas algumas opções. <br>
#### Passo 2: <br>
   • Va ate o a opção "Run As". <br>
#### Passo 3: <br>
   • Selecione a opção "5 Maven Build..." <br>
        
#### Esta imagem mostra os passos 1,2 e 3. <br>

![sonar](sonar.png)

#### Passo 4: <br>
   • Ao selecione a opção "5 Maven Build...! Será exibida a tela como mostra a imagem abaixo.<br>
  
![Mavem Build ...](buildMaven.PNG)
  
#### Passo 5:<br>
   • Note que na imagem acima o botão "Add..." está cirluado.<br>
#### Passo 6:<br>
   • Clique no label "Goals" e insira o seguinte valor org.sonarsource.scanner.maven:sonar-maven-plugin:3.3.0.603:sonar;<br>
    
   ![goals](goals.PNG)
  
#### Passo 7:<br>
   • Clique em "Add..." e a seguinte tela será exibida. <br/>
   • Insira as seguintes propriedades.<br>
   
   Propriedade: sonar.host.url
   <br>Valor: http://seuIP:9000/
   
   Propriedade-> sonar.login
   <br>Valor: seu usuario
   
   Propriedade-> sonar.password
   <br>Valor: senha senha<br>
   
   No final deve ficar algo parecido com a imagem abaixo <br>

   ![goals](add.PNG)
  
Passo 8: <br>
   • Adicionado as as propriedades clique em Apply e depois m Run.<br>
  
### Configurar Jacoco
#### Passo 1:<br>
   • Vá ate o seu projeto e clique bom o botão direito sobre ele. Será exibidas algumas opções.<br>
 #### Passo 2:<br>
   • Va ate o a opção "Run As".<br>
 #### Passo 3:<br>
   • Selecione a opção "5 Maven Build..."<br>
        
  #### Esta imagem mostra os passos 1, 2 e 3.

   ![sonar](sonar.png)

#### Passo 4:<br>
   • Ao selecione a opção "5 Maven Build...! Será exibida a tela como mostra a imagem abaixo.<br>
  
   ![Mavem Build ...](buildMaven.PNG)
  
#### Passo 5:<br>
   • Note que na imagem acima o botão "Add..." está cirluado.<br>
#### Passo 6:<br>
   • Clique no label "Goals" e insira o seguinte valor org.jacoco:jacoco-maven-plugin:prepare-agent verify<br>

![goals](gols2.PNG)

#### Passo 7:<br>
• Clique em "Add..." e a seguinte tela será exibida. <br>
• Insira as seguintes propriedades. <br>

Propriedade: surefire.useFile 
<br>Valor: false   

Propriedade: skip.failsafe.tests 
<br>Valor:true 
   
   No final deve ficar algo parecido com a imagem abaixo <br>

![goals](jacoco.PNG)
  
#### Passo 8: <br>
   • Adicionado as as propriedades clique em Apply e depois m Run.<br>
  
### 'Plugin sonarLint'
#### Passo 1:<br>
   • Abra o eclipse<br> 
#### Passo 2:<br>  
   • Procure na barra de ferramentas o opção Help e clique no mesmo.<br> 
   Esta imagem contepla os passos 1 e 2

![sonarlint01](sonarlint01.PNG)
   
#### Passo 3:<br>  
   • Selecione a opção install new software. Uma nova janela se abrirá.<br> 
   Como esta na imagem

![sonarlint02](sonarlint02.PNG)

#### Passo 4:<br>  
  • Insira o valor no label "Work with": SonarLint for Eclipse Update Site - https://eclipse-uc.sonarlint.org <br>

![sonarlint04](sonarlint03.PNG)

#### Passo 5:<br>
• Após inserir o  valor em "Work with".Para finalizar e so next,next e finish
  ![sonarlint04](sonarlint04.PNG)

  <h1 align="center">
       Utlização dos protocolos devem seguir o padrão abaixo.
   </h1>
   
<p align="center">
   <a href="#protocolos">Protocolos</a> •
   <a href="#verbos">Verbos</a>
</p>

## Protocolos
### HTTP 200:<br>
• Deve ser usado para consultas que tenha algum retorno : 200 ok <br>
      
#### HTTP 201:<br>
• Deve ser usado persistencia de dados com sucesso : 201 create <br>

#### HTTP 204:<br>
• Deve ser usado para consultas que não encontrou um determinado valor no banco : 204 no content <br>
      
#### HTTP 409:<br>
• Ficou definido no hanlde excption como aviso de regra de negocio não atendida. 409 no conflit <br>

#### HTTP 401 <br>
• Acesso negado sem autorização. 401 Unauthorized <br>  

#### HTTP 500 <br>
• Erro sem causa mapeada. 500 Internal Server Error <br>  

## Verbos<BR>
• GET uma representação do recurso de destino;<BR>
• HEAD a mesma representação que GET, mas sem os dados de representação;<BR>
• POST uma representação do status ou resultados obtidos da ação;<BR>
• PUT ou DELETE uma representação do status da ação;<BR>
• OPTIONS uma representação das opções de comunicação;<BR>
• TRACE uma representação da mensagem de solicitação recebida pelo servidor final.<BR>

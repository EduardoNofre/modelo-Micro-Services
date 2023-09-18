## Support & Feedback<BR>
Este projeto é mantido por Eduardo Nofre. Por favor, entenda que não poderemos fornecer suporte individual por e-mail. Acredito também que a ajuda é muito mais valiosa se for partilhada publicamente, para que mais pessoas possam beneficiar dela.

## modelo-Micro-Services<BR>

Modelo de micro services para uso no dia  a dia.
Tem como objetivo servi como um modelo de construção de micro serviço Java. Um padrão a ser seguido.

<p align="center">
   <a href="#ambiente-dev-backend">Ambiente Backend</a> •
   <a href="#infra-estrutura-aws">Ide Eclipse</a> •
  <a href="#ambiente-dev-front">Ambiente Front</a>
</p>

## `Requisito para o desenvolvimento Backend`
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

## `Ide Eclipse`
### Configurar sonar no eclipse<br>
     Passo 1:<br>
        • Vá ate o seu projeto e clique bom o botão direito sobre ele. Será exibidas algumas opções.<br>
     Passo 2:<br>
        • Va ate o a opção "Run As".<br>
     Passo 3:<br>
        • Selecione a opção "5 Maven Build..."<br>
        
  #### Esta imagem mostra os passos 1,2 e 3.

![sonar](sonar.png)

     Passo 4:<br>
        • Ao selecione a opção "5 Maven Build...! Será exibida a tela como mostra a imagem abaixo.<br>
  
     ![Mavem Build ...](buildMaven.PNG)
  
     Passo 5:<br>
        • Note que na imagem acima o botão "Add..." está cirluado.<br>
     Passo 6:<br>
        • Clique no label "Goals" e insira o seguinte valor org.sonarsource.scanner.maven:sonar-maven-plugin:3.3.0.603:sonar;<br>
    
   ![goals](goals.PNG)
  
     Passo 7:<br>
        • Clique em "Add..." e a seguinte tela será exibida. <br>
        • Insira as seguintes propriedades. <br>
            sonar.host.url  http://seuIP:9000/ <br>
            sonar.login seu usuario <br>
            sonar.password senha senha <br>            
        No final deve ficar algo parecido com a imagem abaixo <br>

   ![goals](add.PNG)
  
   Passo 8: <br>
       • Adicionado as as propriedades clique em apply e depois m Run.<br>
  
### Configurar Jacoco
 Passo 1:<br>
        • Vá ate o seu projeto e clique bom o botão direito sobre ele. Será exibidas algumas opções.<br>
     Passo 2:<br>
        • Va ate o a opção "Run As".<br>
     Passo 3:<br>
        • Selecione a opção "5 Maven Build..."<br>
        
  #### Esta imagem mostra os passos 1,2 e 3.

   ![sonar](sonar.png)

     Passo 4:<br>
        • Ao selecione a opção "5 Maven Build...! Será exibida a tela como mostra a imagem abaixo.<br>
  
     ![Mavem Build ...](buildMaven.PNG)
  
     Passo 5:<br>
        • Note que na imagem acima o botão "Add..." está cirluado.<br>
     Passo 6:<br>
        • Clique no label "Goals" e insira o seguinte valor org.jacoco:jacoco-maven-plugin:prepare-agent verify<br>

   ![goals](gols2.PNG)

  Passo 7:<br>
        • Clique em "Add..." e a seguinte tela será exibida. <br>
        • Insira as seguintes propriedades. <br>
               surefire.useFile false <br>
               skip.failsafe.tests true   <br>     
        No final deve ficar algo parecido com a imagem abaixo <br>

   ![goals](jacoco.PNG)
  
   Passo 8: <br>
       • Adicionado as as propriedades clique em apply e depois m Run.<br>
  
### Plugin sonarLint

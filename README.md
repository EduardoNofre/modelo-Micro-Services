## Support & Feedback<BR>
Este projeto é mantido por Eduardo Nofre. Por favor, entenda que não poderemos fornecer suporte individual por e-mail. Acredito também que a ajuda é muito mais valiosa se for partilhada publicamente, para que mais pessoas possam beneficiar dela.

## modelo-Micro-Services
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
- Configurar sonar eclipse
     Passo 1:
        • Vá ate o seu projeto e clique bom o botão direito sobre ele. Será exibidas algumas opções.<br>
     Passo 2:
        • Va ate o a opção "Run As"<br>
     Passo 3:
        • Selecione a opção "5 Maven Build..."<br>
        
  #### Esta imagem mostra os passos 1,2 e 3.

     ![sonar](sonar.png)

     Passo 4:<br>
        • Ao selecione a opção "5 Maven Build...! Será exibida a tela como mostra a imagem abaixo.
  
     ![Mavem Build ...](buildMaven.PNG)
  
     Passo 5:<br>
        • Note que na imagem acima o botão "Add..." está cirluado 
     Passo 6:<br>
        • Clique no label "Goals" e insira o seguinte valor *org.sonarsource.scanner.maven:sonar-maven-plugin:3.3.0.603:sonar*;

    ![goals](goals.PNG)
  
     Passo 7:<br>
        • Clique em "Add..." e a seguinte tela será exibida.

        
  
- Configurar Jacoco
- Plugin sonarLint

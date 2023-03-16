# Projeto da Web Java usando o repositório Maven

###### Este é um projeto feito para cadastrar os moradores do condomínio, a ideia é tornar a vida dos condôminos mais fácil e segura, pois ao se cadastrar na plataforma é gerada uma senha de segurança para que os que entram no condomínio tenham autonomia para reconhecer quem entra e quem sai.

* Escolha uma IDE
1. configurar os servidores (Toncat ou glassfish)

###### Para funcionar, basta clonar o repositório e entrar no repositório configure hibernate.cfg.xml para configurar a senha do seu banco mysql local. próximo passo é criar um banco de dados no mysql (criar banco de dados ordinance;), depois executar o hibernateTeste.ja para criar as tabelas no banco, para finalizar execute o projeto.
----------------------------------------------------------------------------

**Technologies used** 
1. Maven
2. Hibernate
3. PrimeFace
4. JSP

--------------------------------------------------------------------------------



```
mvn archetype:generate \
  -DarchetypeGroupId=org.apache.maven.archetypes \
  -DarchetypeArtifactId=maven-archetype-quickstart \
  -Dversion=1.0-SNAPSHOT \
  -DgroupId=com.erkobridee.exemplo.mvn \
  -DartifactId=ExemploMavenDesktop
```

preparar o projeto para o eclipse

```
mvn eclipse:eclipse 
```


### web java

```
mvn archetype:generate \
    -DarchetypeGroupId=org.apache.maven.archetypes \
    -DarchetypeArtifactId=maven-archetype-webapp \
    -Dversion=1.0-SNAPSHOT \
    -DgroupId=com.erkobridee.exemplo.mvn \
    -DartifactId=ExemploMavenWeb
```

preparar o projeto para o eclipse

```
mvn eclipse:eclipse -Dwtpversion=2.0
```

## Comandos para utilizar em projeto

mostra a arvore de dependencies(.jar)

	mvn depedency:tree 

copia os jar(dependencies) para pasta target/dependency [ evita eventuais problemas de ambiente ]

	mvn dependency:copy-dependencies

compile o projeto

	mvn compile

executa os testes

	mvn test 

gerar os .jars , muito usado em projetos ear

	mvn package 

limpa todas as dependencies(.jars)

	mvn clean 

procura todos os comandos que vc deu para o maven

	history | grep mvn 

boa prática adotada para gerar o pacote de deploy do projeto

	mvn clean install

# Repo Maven Public Idevoc
![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)

### [Como enviar sua Lib](https://mvn.idevoc.com.br/howtosendlib)

### Adicione o repositório ao seu pom.xml

```sh
<repositories>
    <repository>
        <id>central</id>
        <url>https://mvn.idevoc.com.br/</url>
    </repository>
</repositories>
```
### Dependências disponíveis

```sh
<dependency>
    <groupId>dlci</groupId>
    <artifactId>dlci</artifactId>
    <version>1.0.0</version>
</dependency>
```
```sh
<dependency>
    <groupId>ivalid</groupId>
    <artifactId>ivalid</artifactId>
    <version>1.0.0</version>
</dependency>
```
```sh
<dependency>
    <groupId>br.com.idevoc</groupId>
    <artifactId>checkcep</artifactId>
    <version>1.0.0</version>
</dependency>
```
```sh
<dependency>
    <groupId>tratimg</groupId>
    <artifactId>tratimg</artifactId>
    <version>1.0.0</version>
</dependency>
```
```sh
<dependency>
    <groupId>runcmd</groupId>
    <artifactId>runcmd</artifactId>
    <version>1.0.0</version>
</dependency>
```
### Features DLCI
- Criptografia de texto
- Criptografia assimétrica + Criptografia proprietária

```sh
// Criptografar
DLCI dlci = new DLCI();
CharactersResponseDTO ciser = dlci.Ciser("text");

// ver mensagem (contem outros métodos)
System.out.println(ciser.getEncryptedString());

// Descriptografar
Characters diser = dlci.Diser(ciser);
System.out.println(diser.getSequence());
```

### Features IVALID
- Validação de CPF
- Validação de CNPJ
- Validação de Inscrição Estadual por Estado
- API de dias úteis

```sh
// Validar CPF (retorno booleano)
boolean cpf = checkCPF("000.000.000-00");

// Validar CNPJ Ex:
boolean cnpj = checkCNPJ("68.064.264/0001-42");

// Validar inscrição estadual Ex:
boolean ie = checkIE("061.308.539.825", "SP");

// Como deve tratar o sábado (true = sábado útil, false = sábado não útil)
Day day = checkDay("01062021", false||true);
```

### Features CHECKCEP
- Retorna as informações de uma cidade ou bairro pelo CEP em um Objeto manipulável

```sh
// Exemplo
Response response = Checkcep.checkCEP("58900000");
System.out.println(response.toString());
```

### Features TRATIMG
- Manipulação de Imagens

```sh
// Instância
Tratimg tratimg = new Tratimg();

// Exemplo de métodos
tratimg.binarizacao();
tratimg.CalcMediana();
tratimg.brilho();
tratimg.contraste();
tratimg.tonsDeCinza();
tratimg.calculaHistograma();
tratimg.calculaHistogramaAcumulado();
tratimg.equalizacao();
tratimg.LeJanela3x3();
tratimg.negativo();
tratimg.paleta();
tratimg.passaAlta();
tratimg.suavizacao();
```

### Features RUNCMD (Versão Alfa)
- Execute comandos CMD de forma fácil pelo java

```sh
// Exemplo
Runcmd.RunCmd("start calc.exe");
```

##### https://idevoc.com.br/

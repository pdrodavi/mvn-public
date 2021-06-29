# Repo Maven Public Idevoc
![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)

#### Adicione o repositório ao seu pom.xml

```sh
<repositories>
    <repository>
        <id>central</id>
            <url>https://mvn.idevoc.com.br/</url>
    </repository>
</repositories>
```
#### Dependências disponíveis

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

##### https://idevoc.com.br/

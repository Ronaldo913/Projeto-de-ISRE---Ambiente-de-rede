# Etapa 01 - Terminal

A partir daqui você aprenderá a configurar e executar um ambiente de rede virtualizada:

## 1.1 - Login 

É necessário, primeiramente, logar no terminal para dá procedimento no projeto.

<img src="Imagens/img1.png" alt="">

##1.2 - Criar pastas

É preciso criar a pasta labredes na raiz / e subpastas:

```
sudo mkdir /labredes //criando a pasta labredes
```

É preciso criar a pasta images dentro de /labredes:

```
cd /labredes //entrando em labredes 
sudo mkdir imagens // criando subpasta images
cd images //entrando em images
sudo mkdir original //criando subpasta original
```

Para verificar basta entrar em original e imputar o comando:

```
cd original
ls -la
```

Agora é preciso criar os diretórios e subdiretórios:

```md
cd /
sudo mkdir labredes/VM
sudo mkdir labredes/VM/913
sudo mkdir labredes/VM/913/<estudante>
```

No lugar de <estudante>, no nosso caso, substituimos pelos os nossos nomes:
  
* No PC 01: ronaldo
* No PC 02: mayara
* No PC 03: philype
* No PC 04: grupo8

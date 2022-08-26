# No terminal das VMs

## 1 - Configuração das NICs

Para que a VMs utilizem a mesma rede interna é necessário acessar as configurações de Rede de cada VM e selecionar o modo ```rede interna``` e definir o nome da rede, vamos escolher ```labredes``` como nome da nossa rede virtual. Utilize o mesmo nome nas duas VMs.

Imagem 01 - Configuração das NICS.

<img src="Imagens/Img02.png" alt="" width=600>

## 2 - Login nas VMs

Entre com as informações:

```
Usuário da VM: administrador
Senha da VM: adminifal
```

## 3 - Configuração estática do endereço IP na interface de rede

- O Ubuntu utiliza um arquivo YAML para configurar as interfaces de rede
- este arquivo se contra na pasta /etc/netplan/

Digite:

```
ifconfig -a
ls -la /etc/netplan
cat /etc/netplan/01-netcfg.yaml
```

Verifique o nome correto do arquivo no seu servidor. No nosso caso, o nome do arquivo é ```01-netcfg.yaml```.

Imagens 02 e 03 - Sequência dos comando acima.

Imagem 02.

<img src="Imagens/img9.jpg" alt="" width=600>

Imagem 03.

<img src="Imagens/img10.jpg" alt="" width=600>

Após o login, nas VMS, é necessário fazer a instalação das ferramentas de rede que precisaremos para dar prosseguimento com o projeto utilizando o comando ```sudo apt install net-tools -y```:

Imagem 04 - Instalação das ferramentas de rede.

<img src="Imagens/img11.jpg" alt="" width=600>

### Nas VMs

Agora, faz-se necessário editar o arquivo ```01-netcfg.yaml```:

```
sudo nano /etc/netplan/01-netcfg.yaml
```

Imagem 05 - Imputando comando de edição.

<img src="Imagens/img12.jpg" alt="" width=600>

Para cada VM, vamos editar o arquivo de acordo com as definições da tabela da página inicial.

Em seguida, aparecerá as seguintes informações na tela:

Imagem 06 - Informações do arquivo 01-netcfg.yaml.

<img src="Imagens/img13.jpg" alt="" width=600>

- Primeira modificação: 

Alterar o gateway padrão: ```192.168.13.113```.

- Segunda modificação: 

Não é bem uma modificação, mas certifique-se que DHCP está false.

- Terceira modificação: 

Devemos modificar o addresses conforme a tabela pré-definida na tela principal. Ele deve ter o seguinte padrão: ```[192.168.13.xxx/28]```. Em cada VM o ```xxx``` vai ser um número diferente, que relembrando, está na tabela. 

Na imagem abaixo está a configuração da VM1 do usuário grupo8:

Imagem 07 - Arquivo 01-netcfg.yaml editado.

<img src="Imagens/img14.jpg" alt="" width=600>

Faça tal...

<img src="Imagens/img15.jpg" alt="" width=600>

Faça tal...

<img src="Imagens/img16.jpg" alt="" width=600>

Faça tal...

<img src="Imagens/antes da img17.png" alt="" width=600>

## 4 - Configuração da rede interna do VirtualBox

Faça tal...

<img src="Imagens/img17.jpg" alt="" width=600>

Faça tal... 

<img src="Imagens/img18.jpg" alt="" width=600>

Faça tal...

<img src="Imagens/img19.jpg" alt="" width=600>

Faça tal...

<img src="Imagens/img20.jpg" alt="" width=600>

Faça tal...

<img src="Imagens/img21.png" alt="" width=600>

## 5 - Testando o ping entre as duas VMs

---
description: Aprendendo mais um pouco
---

# Aprofundando em Assembly

{% hint style="danger" %}
Esta parte do livro ainda está sendo escrita. Tópicos podem estar fora de ordem ou com informações incompletas.
{% endhint %}

Agora temos conhecimento o bastante para entender como um código em Assembly funciona e porque é importante estudar diversos assuntos relacionados ao sistema operacional, formato do binário e a arquitetura em si para poder programar em Assembly.

Mas vimos tudo isso com código rodando sobre um sistema operacional em submodo 64-bit.  
A ideia desta parte do livro é focar menos nas características do sistema operacional e mais nas características da própria arquitetura.  
Para isso vamos testar código de 64, 32 e 16 bit.

### Ferramentas

Se certifique de ter o [Dosbox](https://www.dosbox.com/) instalado no seu sistema ou qualquer outro emulador do MS-DOS que você saiba utilizar.  
Sistemas compatíveis com o MS-DOS, como o [FreeDOS](http://freedos.org/) por exemplo também podem ser utilizados.

Também é importante que o seu GCC possa compilar código para 64 e 32 bit.  
Em um Linux x86-64 ao instalar o **gcc** você já pode compilar código de 64 bit. Para compilar para 32 bit basta instalar o pacote **gcc-multilib**. No Debian você pode fazer:

```text
$ sudo apt install gcc-multilib
```

No Windows basta instalar o [Mingw-w64](https://mingw-w64.org/doku.php) como já mencionei.

Para testar se está funcionando adequadamente, você pode passar para o GCC a opção **-m32** para compilar para 32 bit.  
Tente compilar um "Hello World" em C e veja se funciona:

```text
$ gcc hello.c -o hello -m32
```

Neste capítulo usaremos também uma ferramenta que vem junto com o nasm, o ndisasm. Ele é um disassembler, um software que converte código de máquina em código Assembly. Se você tem o nasm instalado, também tem o ndisasm disponível.  
O uso básico é só especificar se as instruções devem ser desmontadas como instruções de 16, 32 ou 64 bits. Por padrão ele desmonta as instruções como de 16 bits. Para mudar isso, basta usar a opção -**b** e especificar os bits. Exemplo:

```text
$ ndisasm -b32 binary
```

Qualquer dúvida pode entrar no grupo e fazer uma pergunta:

* [FreeDev - Grupo no Facebook](https://www.facebook.com/groups/fdcasm/)


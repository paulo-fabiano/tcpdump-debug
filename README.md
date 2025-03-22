# Debugando Problemas com o TcpDump

## 1.0 O que é o tcpdump

O `tcpdump` é uma ferramenta de linha de comando que permite analisar os pacotes de rede, com ele podemos diagnosticar, inspecionar e identificar problemas de rede.

## 2.0 Instalando o tcpdump

O pacote que contém o `tcpdump` é o tcpdump (ô Paulo, eu sei rsrs). Para fazermos a instalação da ferramenta usamos o gerenciador de pacotes especifico da distribuição que estamos utilizando.

- Distribuições baseadas em Debian

```
sudo apt install tcpdump
```

- Para fazer o Download em outras distribuições é só usar o gerenciador de pacotes da distruição.

```
sudo <gerenciador-de-pacotes> install tcpdump
```

## 3.0 Usando o tcpdump

- Para capturarmos os pacotes de uma interface de rede especifica:
```
tcpdump -i eth0
```
- Para capturarmos pacotes de um host especifico:

```
tcpdump -i eth0 host 192.168.122.32
```

Confira uma lista com alguns comandos no site da Bosón Treinamentos

- [Tcpdump – Capturar e analisar tráfego de rede no Linux ](https://www.bosontreinamentos.com.br/redes-computadores/tcpdump-capturar-e-analisar-trafego-de-rede-no-linux/)

## 4.0 Casos de uso

O tcpdump é uma ferramenta útil quando pensamos em diagnosticar problemas, principalmente problemas em ambientes de produção. Imagine a situação onde uma aplicação não consegue acessar o servidor do banco de dados. Com o auxílio do `tcpdump` podemos fazer uma analíse inicial e identificar possível problemas com a rede, seja por quê a porta do servidor de banco de dados não tem nenhum serviço rodando, ou por quê há algum firewall bloqueando o tráfego.

### Comandos para diagnóstico

Supondo que o servidor do banco de dados esteja rodando em um servidor com IP 192.168.100.20.

```
tcpdump -i eth0 dst 192.168.100.20
```

Filtramos os pacotes que tem como destino o endereço IP do servidor do banco de dados. Com os pacotes filtrados podemos ver se a conexão TCP é ou não é estabelicida. 

Há algumas variáveis que devemos considerar, mas por hora não irei exemplicar muito aqui.

## Conclusão

Para concluir, o `tcpdump` é uma ótima ferramenta para nos auxiliar na resolução de problemas do dia a dia. Caso tenha chegado até aqui, espero que tenha gostado! Em breve teremos atualziações por aqui.

## Dúvidas ou Sugestões?

Entre em contato comigo via:

- [Linkedin](https://www.linkedin.com/in/paulo-fabiano)
- [Email](mailto:pfabianof@gmail.com)

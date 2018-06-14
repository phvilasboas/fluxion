![Fuxion logo](https://github.com/FluxionNetwork/fluxion/raw/master/logos/logo.jpg)

# Fluxion é o futuro dos ataques MITM WPA
O Fluxion é uma ferramenta de auditoria de segurança e pesquisa em engenharia social. É um remake de linset por vk496 com (esperançosamente) menos bugs e mais funcionalidade. O script tenta recuperar a chave WPA/WPA2 de um ponto de acesso de destino por meio de um ataque de engenharia social (phishing). É compatível com a última versão do Kali (rolling). A configuração dos ataques do Fluxion é principalmente manual, mas o modo automático experimental lida com alguns dos parâmetros de configuração dos ataques. Leia o [FAQ] (https://github.com/phvilasboas/fluxion/wiki/FAQ) antes de solicitar problemas.

## Instalação
Leia [aqui](https://github.com/phvilasboas/fluxion/wiki/Generate-ssh-keys)antes de você fazer os seguintes passos.
<br>
**Download da Última Versão**
```
git clone --recursive git@github.com:phvilasboas/fluxion.git 
```
**Mudar para o diretório da ferramenta**
```
cd fluxion 
```
**Execute o fluxion (as dependências ausentes serão instaladas automaticamente)**
```
./fluxion.sh
```

**Fluxion também está disponível no arch Linux** 
```
cd bin/arch
makepkg
```
ou usando o repositório blackarch
```
pacman -S fluxion
```

## :scroll: Changelog
Fluxion gets weekly updates with new features, improvements, and bugfixes.
Be sure to check out the [changelog here](https://github.com/FluxionNetwork/fluxion/commits/master).

## :Como contribuir
Todas as contribuições são bem vindas! Código, documentação, gráficos ou mesmo sugestões de design são bem-vindos; use o GitHub ao máximo. Envie pedidos pull, contribua com tutoriais ou outro conteúdo wiki - o que quer que você tenha a oferecer, será bem-vindo, mas siga o [style guide] (https://github.com/phvilasboas/fluxion/wiki/Code-style- guia).

## :Livro: Como funciona
* Procure uma rede sem fio alvo.
* Inicie o ataque `Handshake Snooper`.
* Capture um aperto de mão (necessário para verificação de senha).
* Lançamento do ataque `Captive Portal`.
* Gere um AP falso (falso), imitando o ponto de acesso original.
* Gere um servidor DNS, redirecionando todas as solicitações para o host do invasor executando o portal cativo.
* Gere um servidor web, servindo o portal cativo, que solicita aos usuários sua chave WPA / WPA2.
* Gere um jammer, autenticando todos os clientes do AP original e atraindo-os para o AP não autorizado.
* Todas as tentativas de autenticação no portal cativo são verificadas no arquivo de handshake capturado anteriormente.
* O ataque terminará automaticamente assim que uma chave correta for enviada.
* A chave será registrada e os clientes poderão se reconectar ao ponto de acesso de destino.

* Para um guia do ataque `Captive Portal`, leia o [Guia de ataque do Captive Portal](https://github.com/FluxionNetwork/fluxion/wiki/Captive-Portal-Attack)

## :heavy_exclamation_mark: Requerimentos

Um sistema operacional baseado em Linux. Nós recomendamos Kali Linux 2 ou Kali rolling. O Kali 2 & rolling suporta as versões mais recentes do aircrack-ng. Recomenda-se uma placa wifi externa.

## :octocat: Credits
1. l3op - contributor
2. dlinkproto - contributor
3. vk496 - developer of linset
4. Derv82 - @Wifite/2
5. Princeofguilty - @webpages and @buteforce
6. Photos for wiki @http://www.kalitutorials.net
7. Ons Ali @wallpaper
8. PappleTec @sites
9. MPX4132 - Fluxion V3
10. phvilasboas- Fluxion BR

* O uso do Fluxion para atacar infraestruturas sem consentimento mútuo prévio pode ser considerado uma atividade ilegal e é altamente desencorajado por seus autores / desenvolvedores. É de responsabilidade do usuário final obedecer todas as leis locais, estaduais e federais aplicáveis. Os autores não assumem nenhuma responsabilidade e não são responsáveis ​​por qualquer uso indevido ou dano causado por este programa.

## Nota
* Cuidado com os sites que fingem estar relacionados com o Projeto Fluxion. Estes podem estar entregando malware.

* O Fluxion **NÃO FUNCIONA** no Subsistema Linux Para o Windows 10, porque o subsistema não permite acesso a interfaces de rede. Qualquer problema relacionado ao mesmo seria **Fechado imediatamente**

## Links
**Fluxion website:** https://phvilasboas.github.io/fluxion/ <br>
**Facebook:** https:/facebook.com/golinuxoficial <br>

#Script_Perca_de_Pacotes

Este script tem como objetivo monitorar a conectividade de 10 IPs diferentes através de pings. Caso a perda média total de pacotes ultrapasse 10% (ou o valor configurado), o script envia um alerta para um chat no Telegram.

Como Usar
Configure as variáveis do Telegram:


1. Substitua XXXXXXXXXXXXXX pelo token do seu bot do Telegram.
2. Substitua XXXXXXXXXXXXXXXX pelo ID do chat.
3. Caso deseje alterar o limite de perda para alerta, edite a variável limitePerda.

Adicione o script em System → Scheduler no Mikrotik e configure para rodar a cada 1 minuto.
Explicações e Ajustes:

    Cálculo de perda por IP:
        O contador de perdas é incrementado em 1 para cada ping que falha, garantindo que a perda seja contabilizada corretamente para cada IP.
        A média de perda por IP é calculada como a porcentagem de pings perdidos em relação ao total de pings enviados, multiplicando o valor por 100.

    Perda média total:
        A perda média total é calculada considerando o número total de pings realizados e o número de pings realizados para cada IP. A fórmula foi corrigida para refletir corretamente a perda média geral.

    Envio da mensagem para o Telegram:
        A URL para o envio de mensagens foi corrigida. As variáveis são convertidas para strings usando [:tostr] e a URL é construída de maneira a garantir que a mensagem seja enviada corretamente.
        A URL é formatada para incluir o emoji e a perda média total, juntamente com o valor de perda em porcentagem.

Agora, o script deve monitorar corretamente a perda de pacotes para os IPs listados e enviar uma mensagem de alerta para o Telegram caso a perda média ultrapasse o limite configurado.

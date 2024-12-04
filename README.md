#Script_Perca_de_Pacotes

Este script tem como objetivo monitorar a conectividade de 10 IPs diferentes através de pings. Caso a perda média total de pacotes ultrapasse 10% (ou o valor configurado), o script envia um alerta para um chat no Telegram.

Como Usar
Configure as variáveis do Telegram:


1. Substitua XXXXXXXXXXXXXX pelo token do seu bot do Telegram.
2. Substitua XXXXXXXXXXXXXXXX pelo ID do chat.
3. Caso deseje alterar o limite de perda para alerta, edite a variável limitePerda.

Adicione o script em System → Scheduler no Mikrotik e configure para rodar a cada 1 minuto.


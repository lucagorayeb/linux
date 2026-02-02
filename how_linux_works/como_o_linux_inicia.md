# Como o sistema inicia

+ Mensagens de inicialização

As informações apresentadas quando o linux liga são pouco informativas 
e o hardware evoluiu tanto que quando aparece alguma mensagem ela 
desaparece muito rápido pois o sistema liga mais rápido do que antes.

Existem duas maneiras de ver o kernel iniciando e as mensagens de 
diagnostico de execução:

 - Olhar no sistema de log do kernel. Geralmente encontrado no /var/log
/kern.log, mas dependendo de como o sistema está configurado pode estar
junto de outros logs do sistema no /var/log/messages ou em outro lugar.

- Usar o comando dmesg, mas tenha certeza de usar o pipe e o comando 
less porque sera um trabalho bem grande. O dmesg usa o buffer sino do 
kernel, que tem tamanho limitado.

+ Inicialização do kernel e opções de boot

O kernel inicia nessa seguinte ordem:

*1 - Inspeção da CPU 
*2 - Inspeção da Memória 
*3 - Descoberta dos dispositivo de bus
*4 - Descoberta de dispositivo 
*5 - Configuração do subsistema auxiliar do kernel (internet e entre outros)
*6 - Montagem do sistema de arquivo do root
*7 - Inicialização do espaço do usuário

+ Parametros do kernel 

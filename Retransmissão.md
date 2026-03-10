# 10/03/26
# Retransmissão

- Ferramenta: Wireshark, sniffer de rede. Captura pacotes e salva eles em arquivos .pcap ou .pcapng (captura de pacotes).

- O que é: Retransmissão é basicamente quando um cliente ou servidor não recebe a confirmação de dados(ACK) de alguns dos lados
  
   - Quando acontece: Acontece quando algo na rede descartou o pacote.
 
      - Pode ser Congestionamento de rede (Muito tráfego ao mesmo tempo)
      - RAM/BUFFER de roteador ou Switch cheios(RAM/BUFFER = armazena os dados recebidos temporariamente).
      - Interferência (cabo ou sinal wi-fi ruins).
      - Firewall dropando(ignorando) pacotes recebidos.
        
   - [!] Existem outras causas, mas para os meus estudos, só essa parte já basta.

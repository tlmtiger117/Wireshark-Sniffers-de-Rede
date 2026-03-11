# 11/03/26
# Filtros Básicos do Wireshark

- Operadores lógicos: Responsáveis por complementar mais de um filtro de uma só vez:
   - "&&" AND/E: Responsável por complementar a lógica de um filtro (adciona outro filtro).
      - AND: Cumpre a mesma função do "&&", só muda a sintáxe.
     
   - "||" OR/OU: Responsável por decidir entre um filtro e outro ("esse filtro, mas se não tiver dados nele, usa esse outro").
     
   - "!"(NOT): Responsável por excluir o tráfego indesejado no snuffer.

- Filtros Básicos:

   - Host específico:	                                ip.addr == 192.168.1.10	Mostra pacotes de/para o host
     
   - Somente origem:                                   ip.src == 192.168.1.10	Apenas pacotes enviados pelo host
     
   - Somente destino:	                                ip.dst == 192.168.1.10	Apenas pacotes recebidos pelo host
     
   - Excluir host:	                                    !(ip.addr == 192.168.1.10)	Ignora o host no tráfego
     
   - Porta TCP específica:	                            tcp.port == 21	Ex: FTP
  
   - Porta TCP origem:	                                tcp.srcport == 21
     
   - Porta TCP destino:	                              tcp.dstport == 21
     
   - Porta UDP específica:	                            udp.port == 53	Ex: DNS
     
   - Protocolo TCP	tcp:	                              Todos pacotes TCP
     
   - Protocolo UDP	udp:	                              Todos pacotes UDP
     
   - Protocolo FTP	ftp:	                              Exibe apenas comandos FTP
     
   - Protocolo HTTP	http:	                            Exibe apenas HTTP
     
   - SYN:	                                            tcp.flags.syn == 1	Pacotes de abertura de conexão
     
   - ACK:	                                            tcp.flags.ack == 1	Pacotes de confirmação
     
   - FIN:	                                            tcp.flags.fin == 1	Finalização de conexão
     
   - RST:	                                            tcp.flags.reset == 1	Pacotes de reset
     
   - SYN + ACK:	                                      tcp.flags.syn == 1 && tcp.flags.ack == 1
     
   - Retransmissão TCP:	                              tcp.analysis.retransmission	Pacotes retransmitidos
     
   - Pacotes fora de ordem:	                          tcp.analysis.out_of_order
     
   - Segmentos perdidos:	                              tcp.analysis.lost_segment
     
   - Conteúdo em texto puro:	                          frame contains localiza linhas em texto puro
 

  
     
  

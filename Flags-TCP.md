# 12/03/26
# Flags-TCP

- SYN (Synchronize): iniciar uma conexão TCP.
   - Quando um cliente quer abrir uma conexão com um servidor, ele envia um pacote com a flag SYN ativa.
   - Em análise de tráfego:
     
      - Indica tentativa de início de conexão
      - Muito usado para detectar scans de porta

- ACK (Acknowledge): Responsável por receber os dados do cliente(aceitar).
   - Quando algum dos lados confirma o recebimente de dados.
  
- FIN (Finish) Função: encerrar a conexão de forma graciosa.
   - Quando um lado terminou de enviar dados, ele manda FIN.

- RST (Reset)Função: encerrar imediatamente a conexão.
   - O RST é enviado quando:
      - A conexão não existe

      - Um host quer abortar a conexão
      - porta fechada
      - Um pacote chega a uma porta sem serviço escutando
      - Filrewall configurado para recusar a conexão(aviso)
      - aplicação abortando sessão(recusando processar os dados)
      - tráfego malformado (pacote TCP faltando conteúdo). O TCP não aceita pacotes faltando coisas
      - 
- PSH(Push)Função:Envio de dados imediato para alguma aplicação(programa), sem esperar o buffer(RAM) da tacela TCP
                  da aplicação acumule mais dados(recebe e já manda rapidamente).

- Flag Significado e Uso principal:

   - SYN	   ->       Synchronize	                ->  Início da conexão
   - SYN+ACK ->	  Synchronize + Acknowledge	 ->  Aceitação da conexão
   - PSH    ->      Push                         -> Manda dados imediatamente(recebeu, armazenou(RAM)mandou).
   - FIN	   ->      Finish	                      ->  Encerramento normal
   - RST	   ->      Reset	                      ->  Encerramento abrupto


     

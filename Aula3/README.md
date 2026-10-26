1. Objetivo: o que foi realizado.
R: Estudos sobre endereço de IP e utilização de aplicativos relacionados a redes

4. Procedimento: comandos executados, em ordem. 
Procedimentos:
	1. ip addr show
	2. ip link
	3. ip route
	4. netplan status

	5. ping -c 4 127.0.0.1
	6. ping -c 4 <IP-da-sua-VM>
        7. ping -c 4 10.0.2.2
	8. ping -c 4 8.8.8.8
	9. ping -c 4 google.com
	
===============================================
pergunta 1.
	nome da interface: enp0s3
 	IP/prefixo: 10.0.2.15/24  IPv6: fd17:625c:f037:2:a00:27ff:fe81:4393/64
	MAC: 08:00:27:81:43:93
 	gateway padrão: 10.0.2.2
pergunta 2.
	O endereço 10.0.2.15 existe apenas dentro de uma rede virtual privada e emulada pelo motor NAT do VirtualBox. O sistema operacional do Host não possui uma interface de rede configurada nessa sub-rede nem uma rota para ela, tornando esse IP inacessível diretamente para a placa física do Host.

pergunta 3.
	R: Não houve problema algum
pergunta 4.
	R: No modo NAT, a VM opera numa sub-rede privada e isolada (10.0.2.15/24), acedendo à rede externa através de um gateway virtual (10.0.2.2). Este funcionamento permite que a VM navegue na Internet, mas impede que o Host aceda diretamente à VM. Para obter comunicação bidirecional direta sem configurar o redirecionamento de portas, deve alterar-se a interface para o modo Bridge


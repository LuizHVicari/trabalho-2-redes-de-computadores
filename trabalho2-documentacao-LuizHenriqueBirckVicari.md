# Trabalho 2: Integração de habilidades - 2022/1
**Disciplina: Redes de Computadores**

**Curso: Engenharia de Computação / Elétrica**

**Luiz Henrique Birck Vicari/2155176:**


## Tarefa 1:  Sub-Redes
| Sub- Rede |             IPv6 - Sub-Rede            |  IPv4 - Sub-Rede  |  IPv4 - Máscara   | IPv4 - Broadcast  |    
|:---------:|:--------------------------------------:|:-----------------:|:-----------------:|:-----------------:|
| Matriz    | 2001:DB8:ACAD:4C00::/64 | 200.200.76.0   | 255.255.255.192 | 200.200.76.63  |
| Filial 1  | 2001:DB8:ACAD:4C01::/64 | 200.200.76.64  | 255.255.255.224 | 200.200.76.95  |
| Filial 2  | 2001:DB8:ACAD:4C02::/64 | 200.200.76.96  | 255.255.255.224 | 200.200.76.127 |
| Filial 3  | 2001:DB8:ACAD:4C03::/64 | 200.200.76.128 | 255.255.255.224 | 200.200.76.159 |
| Filial 4  | 2001:DB8:ACAD:4C04::/64 | 200.200.76.160 | 255.255.255.224 | 200.200.76.192 |
| Filial 5  | 2001:DB8:ACAD:4C05::/64 | 200.200.76.192 | 255.255.255.224 | 200.200.76.223 |
| pb-vit    | 2001:DB8:ACAD:4CFF::0:0/112 | 200.200.76.224 | 255.255.255.252 | 200.200.76.227 |
| vit-fb    | 2001:DB8:ACAD:4CFF::1:0/112 | 200.200.76.228 | 255.255.255.252 | 200.200.76.231 |
| fb-ita    | 2001:DB8:ACAD:4CFF::2:0/112 | 200.200.76.232 | 255.255.255.252 | 200.200.76.235 |
| ita-pb    | 2001:DB8:ACAD:4CFF::3:0/112 | 200.200.76.236 | 255.255.255.252 | 200.200.76.239 |
| cv-ita    | 2001:DB8:ACAD:4CFF::4:0/112  | 200.200.76.240 | 255.255.255.252 | 200.200.76.243 |


## Tarefa 2: Endereçamento de Dispositivos
| Dispositivo|Interface| IPv4          |IPv4 - Máscara |IPv4 - Gateway| IPv6/Prefixo            |IPv6 - Gateway           |
|:------------:|:---------:|:---------------:|:---------------:|:--------------:|:---------------------------|:-------------------------:|
| PC1        | NIC     |200.200.76.3   |255.255.255.192|200.200.76.1  |2001:DB8:ACAD:4C00::03/64  |2001:DB8:ACAD:4C00::01/64|
| PC2        | NIC     |200.200.76.4   |255.255.255.192|200.200.76.1  |2001:DB8:ACAD:4C00::04/64  |2001:DB8:ACAD:4C00::01/64|
| PC3        | NIC     |200.200.76.67  |255.255.255.224|200.200.76.65 |2001:DB8:ACAD:4C01::03/64  |2001:DB8:ACAD:4C01::01/64|
| PC4        | NIC     |200.200.76.68  |255.255.255.224|200.200.76.65 |2001:DB8:ACAD:4C01::04/64  |2001:DB8:ACAD:4C01::01/64|
| PC5        | NIC     |200.200.76.99  |255.255.255.224|200.200.76.97 |2001:DB8:ACAD:4C02::03/64  |2001:DB8:ACAD:4C02::01/64|
| PC6        | NIC     |200.200.76.100 |255.255.255.224|200.200.76.97 |2001:DB8:ACAD:4C02::04/64  |2001:DB8:ACAD:4C02::01/64|
| Switch-Matriz | SVI   |200.200.76.2  |255.255.255.192|200.200.76.1  |                           |                         |
| Switch-Filial1 | SVI  |200.200.76.66 |255.255.255.224|200.200.76.65 |                           |                         |
| Switch-Filial2 | SVI  |200.200.76.98 |255.255.255.224|200.200.76.97 |                           |                         |
| Roteador-Pato Branco  | Fa0/0 |200.200.76.1  |255.255.255.192|      |2001:DB8:ACAD:4C00::1/64   |                         |
| Roteador-Pato Branco  |Se0/0/0|200.200.76.225|255.255.255.252|      |2001:DB8:ACAD:4CFF::1/112  |                         |
| Roteador-Pato Branco  |Se0/0/1|200.200.76.238|255.255.255.252|      |2001:DB8:ACAD:4CFF::3:2/112|                         |
| Roteador-Fco. Beltrão |Fa0/0  |200.200.76.65 |255.255.255.224|      |2001:DB8:ACAD:4C01::0:1/64 |                         |
| Roteador-Fco. Beltrão |Se0/0/0|200.200.76.233|255.255.255.252|      |2001:DB8:ACAD:4CFF::2:1/112|                         |
| Roteador-Fco. Beltrão |Se0/0/1|200.200.76.230|255.255.255.252|      |2001:DB8:ACAD:4CFF::1:2/112|                         |
| Roteador-Vitorino     |Se0/0/0|200.200.76.229|255.255.255.252|      |2001:DB8:ACAD:4CFF::1:1/112|                         |
| Roteador-Vitorino     |Se0/0/1|200.200.76.226|255.255.255.252|      |2001:DB8:ACAD:4CFF::2/112  |                         |
| Roteador-Itapejara    |Se0/0/0|200.200.76.237|255.255.255.252|      |2001:DB8:ACAD:4CFF::3:1/112|                         |
| Roteador-Itapejara    |Se0/0/1|200.200.76.234|255.255.255.252|      |2001:DB8:ACAD:4CFF::2:2/112|                         |
| Roteador-Itapejara    |Fa0/1  |200.200.76.241|255.255.255.252|      |2001:DB8:ACAD:4CFF::4:1/112|                         |
| Roteador-Coronel      |Fa0/0  |200.200.76.197|255.255.255.224|      |2001:DB8:ACAD:4C02::1/64   |                         |
| Roteador-Coronel      |Fa0/1  |200.200.76.242|255.255.255.252|      |2001:DB8:ACAD:4CFF::4:2/112|                         |

## Tarefa 3: Tabela de Roteamento
### Roteador Pato Branco
#### IPv4
| Rede de Destino | Máscara       | Next Hop     | Interface de Saída |
|:---------------:|:---------:    |:------:      |:------------:      |
|200.200.76.64    |255.255.255.224|200.200.76.226|se0/0/0             |
|200.200.76.96    |255.255.255.224|200.200.76.226|se0/0/0             |
|200.200.76.228   |255.255.255.252|200.200.76.226|se0/0/0             |
|200.200.76.232   |255.255.255.252|200.200.76.226|se0/0/0             |
|200.200.76.240   |255.255.255.252|200.200.76.226|se0/0/0             |
#### IPv6
| Rede de Destino/Prefixo   | Next Hop            | Interface de Saída |
|:-----------------:        |:----------:         |:------------------:|
|2001:db8:acad:4C01::/64    |2001:db8:acad:4cff::2|se0/0/0             |
|2001:db8:acad:4C02::/64    |2001:db8:acad:4cff::2|se0/0/0             |
|2001:db8:acad:4Cff::1:0/112|2001:db8:acad:4cff::2|se0/0/0             |
|2001:db8:acad:4Cff::2:0/112|2001:db8:acad:4cff::2|se0/0/0             |
|2001:db8:acad:4Cff::4:0/112|2001:db8:acad:4cff::2|se0/0/0             |

### Roteador Coronel Vivida
#### IPv4
| Rede de Destino | Máscara       | Next Hop     | Interface de Saída |
|:---------------:|:---------:    |:------:      |:------------:      |
|200.200.76.0     |255.255.255.192|200.200.76.241|fa0/1               |
|200.200.76.64    |255.255.255.224|200.200.76.241|fa0/1               |
|200.200.76.224   |255.255.255.252|200.200.76.241|fa0/1               |
|200.200.76.228   |255.255.255.252|200.200.76.241|fa0/1               |
|200.200.76.232   |255.255.255.252|200.200.76.241|fa0/1               |
|200.200.76.236   |255.255.255.252|200.200.76.241|fa0/1               |
#### IPv6
| Rede de Destino/Prefixo   | Next Hop             | Interface de Saída |
|:-----------------:        |:----------:          |:------------------:|
|2001:db8:acad:4C00::/64    |2001:db8:acad:4cff:4:1|fa0/1               |
|2001:db8:acad:4C01::/64    |2001:db8:acad:4cff:4:1|fa0/1               |
|2001:db8:acad:4Cff::/112   |2001:db8:acad:4cff:4:1|fa0/1               |
|2001:db8:acad:4Cff::1:0/112|2001:db8:acad:4cff:4:1|fa0/1               |
|2001:db8:acad:4Cff::2:0/112|2001:db8:acad:4cff:4:1|fa0/1               |
|2001:db8:acad:4Cff::3:0/112|2001:db8:acad:4cff:4:1|fa0/1               |

### Roteador Itapejara D'Oeste
#### IPv4
| Rede de Destino | Máscara       | Next Hop     | Interface de Saída |
|:---------------:|:---------:    |:------:      |:------------:      |
|200.200.76.0     |255.255.255.192|200.200.76.238|se0/0/0             |
|200.200.76.64    |255.255.255.224|200.200.76.238|se0/0/0             |
|200.200.76.96    |255.255.255.224|200.200.76.242|fa0/1               |
|200.200.76.224   |255.255.255.252|200.200.76.238|se0/0/0             |
|200.200.76.228   |255.255.255.252|200.200.76.238|se0/0/0             |

#### IPv6
| Rede de Destino/Prefixo   | Next Hop             | Interface de Saída |
|:-----------------:        |:----------:          |:------------------:|
|2001:db8:acad:4C00::/64    |2001:db8:acad:4cff:3:2|se0/0/0             |
|2001:db8:acad:4C01::/64    |2001:db8:acad:4cff:3:2|se0/0/0             |
|2001:db8:acad:4C02::/64    |2001:db8:acad:4cff:4:2|fa0/1               |
|2001:db8:acad:4Cff::/112   |2001:db8:acad:4cff:3:2|se0/0/0             |
|2001:db8:acad:4Cff::1:0/112|2001:db8:acad:4cff:3:2|se0/0/0             |

### Roteador Vitorino
#### IPv4
| Rede de Destino | Máscara       | Next Hop     | Interface de Saída |
|:---------------:|:---------:    |:------:      |:------------:      |
|200.200.76.0     |255.255.255.192|200.200.76.230|se0/0/0             |
|200.200.76.64    |255.255.255.224|200.200.76.230|se0/0/0             |
|200.200.76.96    |255.255.255.224|200.200.76.230|se0/0/0             |
|200.200.76.232   |255.255.255.252|200.200.76.230|se0/0/0             |
|200.200.76.236   |255.255.255.252|200.200.76.230|se0/0/0             |
|200.200.76.240   |255.255.255.252|200.200.76.230|se0/0/0             |

#### IPv6
| Rede de Destino/Prefixo   | Next Hop             | Interface de Saída |
|:-----------------:        |:----------:          |:------------------:|
|2001:db8:acad:4C00::/64    |2001:db8:acad:4cff:1:2|se0/0/0             |
|2001:db8:acad:4C01::/64    |2001:db8:acad:4cff:1:2|se0/0/0             |
|2001:db8:acad:4C02::/64    |2001:db8:acad:4cff:1:2|se0/0/0             |
|2001:db8:acad:4Cff::2:0/112|2001:db8:acad:4cff:1:2|se0/0/0             |
|2001:db8:acad:4Cff::3:0/112|2001:db8:acad:4cff:1:2|se0/0/0             |
|2001:db8:acad:4Cff::4:0/112|2001:db8:acad:4cff:1:2|se0/0/0             |

### Roteador Francisco Beltrão
#### IPv4
| Rede de Destino | Máscara       | Next Hop     | Interface de Saída |
|:---------------:|:---------:    |:------:      |:------------:      |
|200.200.76.0     |255.255.255.192|200.200.76.234|se0/0/0             |
|200.200.76.96    |255.255.255.224|200.200.76.234|se0/0/0             |
|200.200.76.224   |255.255.255.252|200.200.76.234|se0/0/0             |
|200.200.76.236   |255.255.255.252|200.200.76.234|se0/0/0             |
|200.200.76.240   |255.255.255.252|200.200.76.234|se0/0/0             |

#### IPv6
| Rede de Destino/Prefixo   | Next Hop             | Interface de Saída |
|:-----------------:        |:----------:          |:------------------:|
|2001:db8:acad:4C00::/64    |2001:db8:acad:4cff:2:2|se0/0/0             |
|2001:db8:acad:4C02::/64    |2001:db8:acad:4cff:2:2|se0/0/0             |
|2001:db8:acad:4Cff::/112   |2001:db8:acad:4cff:2:2|se0/0/0             |
|2001:db8:acad:4Cff::3:0/112|2001:db8:acad:4cff:2:2|se0/0/0             |
|2001:db8:acad:4Cff::4:0/112|2001:db8:acad:4cff:2:2|se0/0/0             |


## Topologia - Packet Tracer
- [ ] ![Trabalho2-Topologia-LuizHenriqueBirckVicari](Trabalho2-Topologia-LuizHenriqueBirckVicari.pkt)


## Arquivos de Configuração dos Dispositivos Intermediários (roteadores e switches)
- [ ] ![Roteador Pato Branco](r-pb-lh.txt)
- [ ] ![Roteador Francisco Beltrão](r-fb-lh.txt)
- [ ] ![Roteador Vitorino](r-vit-lh.txt)
- [ ] ![Roteador Itapejara D'Oeste](r-ita-lh.txt)
- [ ] ![Roteador Coronel Vivida](r-cv-lh.txt)
- [ ] ![Switch Pato Branco](sw-matriz-lh.txt)
- [ ] ![Switch Francisco Beltrão](sw-filial1-lh.txt)
- [ ] ![Switch Coronel Vivida](sw-filial2-lh.txt)



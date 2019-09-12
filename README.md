# -GameboyHackrom
#### Edição de ROM de gameboy para a matéria de Interface Hardware/Software na UFS
Iniciei pela edição de texto. Como podemos ver, ao buscar com um editor de HEX algum termo do jogo, não achamos nada.
![1](https://raw.githubusercontent.com/VictorLFR/-GameboyHackrom/master/1.png)
Isso ocorre porque nas ROMs de gameboy ao invés de ter caracteres convencionais ele usa a própria tabela de caracteres, como mostrado abaixo:
![2](https://raw.githubusercontent.com/VictorLFR/-GameboyHackrom/master/2.png)
A partir daí criei um conversor simples, que está aqui nesse git, chamado "conversor.py". E consegui achar o dado que queria e modificar e mudar o valor dele:
__playing the SNES = AF AB A0 B8 A8 AD A6 7F B3 A7 A4 7F 92 8D 84 92
fzd trab de IHS = A5 B9 A3 7F B3 B1 A0 A1 7F A3 A4 7F 88 87 92__
![3](https://raw.githubusercontent.com/VictorLFR/-GameboyHackrom/master/3.png)
Procurando no manual do processador do gameboy consegui achar recomendações de onde os Tiles do gameboy estão na ROM e consegui descobrir observando os padrões e testando modificar aonde estavam os Tiles de Pallet Town(em 0x182FD começam os tile maps), a primeira cidade do jogo.
Então modifiquei os Tiles referentes a casa do professor carvalho e o resultado pode ser visto em jogo.
![4](https://raw.githubusercontent.com/VictorLFR/-GameboyHackrom/master/4.png)
![5](https://raw.githubusercontent.com/VictorLFR/-GameboyHackrom/master/5.png)
Para ver os resultado, obtenha legalmente a ROM do Pokemon Red USA com SHA-1 = 1ED352E5AB1B89AA9664CFF8111AEF7D89C9F8AB e aplique o patch "Pokemon Red MOD.ips" com o programa LunarIPS.

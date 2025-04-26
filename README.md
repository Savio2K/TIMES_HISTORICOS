# Dados dos times históricos
times_historicos = {
    "Brasil 1970": {
        "Técnico": "Mário Zagallo",
        "Formação": "4-4-2",
        "Jogadores": [
            "Félix (GOL)",
            "Carlos Alberto (LD)",
            "Britto (ZAG)",
            "Piazza (ZAG)",
            "Everaldo (LE)",
            "Clodoaldo (VOL)",
            "Gérson (MC)",
            "Rivelino (ME)",
            "Jairzinho (MD)",
            "Pelé (ATA)",
            "Tostão (ATA)"
        ]
    },
    "Barcelona 2009": {
        "Técnico": "Pep Guardiola",
        "Formação": "4-3-3",
        "Jogadores": [
            "Valdés (GOL)",
            "Puyol (LD)",
            "Piqué (ZAG)",
            "Yaya Touré (ZAG)",
            "Sylvinho (LE)",
            "Xavi (MC)",
            "Busquets (VOL)",
            "Iniesta (MC)",
            "Messi (PD)",
            "Eto'o (ATA)",
            "Henry (PE)"
        ]
    },
    "Real Madrid 2017": {
        "Técnico": "Zinedine Zidane",
        "Formação": "4-3-1-2",
        "Jogadores": [
            "Keylor Navas (GOL)",
            "Carvajal (LD)",
            "Ramos (ZAG)",
            "Varane (ZAG)",
            "Marcelo (LE)",
            "Modrić (MC)",
            "Casemiro (VOL)",
            "Kroos (MC)",
            "Isco (MEI)",
            "Benzema (ATA)",
            "Cristiano Ronaldo (ATA)"
        ]
    },
    "Barcelona 2015": {
        "Técnico": "Luis Enrique",
        "Formação": "4-4-3",
        "Jogadores": [
            "Ter Stegen (GOL)",
            "Dani Alves (LD)",
            "Piqué (ZAG)",
            "Mascherano (ZAG)",
            "Jordi Alba (LE)",
            "Iniesta (MC)",
            "Busquets (VOL)",
            "Rakitic (MC)",
            "Messi (PD)",
            "Suarez (ATA)",
            "Neymar (PE)"
        ]
    },
    "Brasil 2002": {
        "Técnico": "Felipão",
        "Formação": "5-3-2",
        "Jogadores": [
            "Marcos (GOL)",
            "Cafu (LD)",
            "Roque Jr (ZAG)",
            "Lúcio (ZAG)",
            "Edmilson (ZAG)",
            "Roberto Carlos (LE)",
            "Gilberto Silva (VOL)",
            "Kleberson (MC)",
            "Ronaldinho (MEI)",
            "Ronaldo (ATA)",
            "Rivaldo (ATA)"
        ]
    },
     "Botafogo 2024": {
        "Técnico": "Artur Jorge",
        "Formação": "4-5-1",
        "Jogadores": [
            "John (GOL)",
            "Vitinho (LD)",
            "Adryelson (ZAG)",
            "Barboza (ZAG)",
            "Alex Telles (LE)",
            "Gregore (VOL)",
            "Marlon Freitas (VOL)",
            "Luiz Henrique (MD)",
            "Savarino (MEI)",
            "Almada (ME)",
            "Igor Jesus (ATA)",
        ]
    },
    "Flamengo 2019": {
        "Técnico": "Jorge Jesus",
        "Formação": "4-5-1",
        "Jogadores": [
            "Diego Alves (GOL)",
            "Rafinha (LD)",
            "Rodrigo Caio (ZAG)",
            "Pablo Marí (ZAG)",
            "Filipe Luis (LE)",
            "Willian Arão (VOL)",
            "Gerson (VOL)",
            "Everton Ribeiro (MD)",
            "Arrascaeta (MEI)",
            "Bruno Henrique (ME)",
            "Gabigol (ATA)",
        ]
    },
    "Milan 2005": {
        "Técnico": "Carlo Ancelotti",
        "Formação": "4-3-1-2",
        "Jogadores": [
            "Dida (GOL)",
            "Cafu (LD)",
            "Stam (ZAG)",
            "Nesta (ZAG)",
            "Maldini (LE)",
            "Pirlo (VOL)",
            "Seedorf (MC)",
            "Gattuso (MC)",
            "Kaká (MEI)",
            "Shevchenko (ATA)",
            "Crespo (ATA)",
        ]
    },
    "Internazionale 2010": {
        "Técnico": "José Mourinho",
        "Formação": "4-5-1",
        "Jogadores": [
            "Júlio César (GOL)",
            "Maicon (LD)",
            "Lúcio (ZAG)",
            "Samuel (ZAG)",
            "Chivu (LE)",
            "Zanetti (VOL)",
            "Cambiasso (VOL)",
            "Eto'o (MD)",
            "Sneijder (MEI)",
            "Pandev (ME)",
            "Milito (ATA)",
        ]
        
    }
    
}

# Função para mostrar escalação
def mostrar_escalacao(time):
    print(f"\n=== {time} ===")
    print(f"Técnico: {times_historicos[time]['Técnico']}")
    print(f"Formação: {times_historicos[time]['Formação']}\n")
    print("Escalação:")
    for jogador in times_historicos[time]["Jogadores"]:
        print(f"• {jogador}")

# Menu principal
while True:
    print("\n=== TIMES HISTÓRICOS ===")
    print("Escolha um time para ver a escalação:")
    for i, time in enumerate(times_historicos.keys(), 1):
        print(f"{i}. {time}")
    print("0. Sair")
    
    opcao = input("\nDigite o número do time: ")
    
    if opcao == "0":
        print("Até logo!")
        break
    elif opcao in ["1", "2", "3","4","5","6","7","8","9"]:
        time_escolhido = list(times_historicos.keys())[int(opcao)-1]
        mostrar_escalacao(time_escolhido)
    else:
        print("Opção inválida. Tente novamente.")

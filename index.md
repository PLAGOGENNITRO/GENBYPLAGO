import random, string, requests, webbrowser, time
f = open("Valid Nitro.txt", "w", encoding='utf-8')

print(
    """GRACIAS POR GENERAR AQUI TE GUTARIA UNIRTE A MI SERVIDOR DE DISCORD TE DEJA LA INVITE AQUI https://discord.gg/hsRKxUEc9U GRACIAS DE VERDAD 

GEN CREADO POR: ✘𝐏𝐋𝐀𝐆𝐎✘#4350


AQUI TUS CODES DE NITRO""")

while True:
    code = ('').join(random.choices(string.ascii_letters + string.digits,
                                    k=16))
    r = requests.get(
        f"https://discordapp.com/api/v6/entitlements/gift-codes/{code}?with_application=false&with_subscription_plan=true"
    )
    if r.status_code == 200:
        print(f"Código Valido > https://discord.gift/{code}")
        f.write(f"https://discord.gift/{code}\n")
    else:
        print(f"Código Invalido > https://discord.gift/{code}")

        #by plago


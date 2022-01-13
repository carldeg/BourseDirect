# BourseDirect
A simple way to execute  Bourse Direct (french broker) orders thanks to python.

To execute an order, please proceed like this : 


(Make sure you wrote your Login and you Pwd as cmd line argument)

Exemple :
'''
order = {

    "ISIN": 'FR0000130809',
    "SENS": 'vente',  # achat ou vente
    "ORDERTYPE": 'stop',  # market, limit, best_limit, stop, stop_limit, tal
    "LIMIT/STOP": 40,
    "PLAGE": {
        'LIMIT': None,  # down
        'STOP': None,  # up
    },
    "QUANTITE": 1,
    "VIRTUAL": 'on',
}


dwd_path = 'C:\\Users\\carld\\OneDrive\\Bureau\\Documents\\ProjetPython\\ClassesPerso\\Termsheet\\'
bd = BourseDirectInfo(Display=True, download_path=dwd_path)
bd.execute(order=order)
bd.close_connection()
'''

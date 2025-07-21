import pandas as pd
import os
import shutil
from tkinter import messagebox, Tk

pasta_base = os.path.dirname(os.path.abspath(__file__))
planilha = os.path.join(pasta_base, "Arquivos a separar.xlsx")
pasta_entrada = os.path.join(pasta_base, "Pdf")
pasta_saida = os.path.join(pasta_base, "Selecionados")

root = Tk()
root.withdraw()

if not os.path.exists(planilha):
    messagebox.showerror("Erro", "Planilha 'Arquivos a separar.xlsx' não encontrada.")
    exit()

if not os.path.exists(pasta_entrada):
    messagebox.showerror("Erro", "Pasta 'Pdf' não encontrada.")
    exit()

df = pd.read_excel(planilha)
numeros_validos = set(df.iloc[:, 0].astype(str))

os.makedirs(pasta_saida, exist_ok=True)

encontrados = 0
for nome_arquivo in os.listdir(pasta_entrada):
    if nome_arquivo.lower().endswith(".pdf"):
        numero = nome_arquivo.replace(".pdf", "").split("_")[-1]
        if numero in numeros_validos:
            origem = os.path.join(pasta_entrada, nome_arquivo)
            destino = os.path.join(pasta_saida, nome_arquivo)
            shutil.copy2(origem, destino)
            encontrados += 1

messagebox.showinfo("Finalizado", f"{encontrados} arquivos separados com sucesso em 'Selecionados'.")

# Analisador-de-Sentimentos
Um programa que analisa o sentimento de um texto usando uma biblioteca de processamento de linguagem natural (NLP).

from textblob import TextBlob

def analisar_sentimento(texto):
    analise = TextBlob(texto)
    if analise.sentiment.polarity > 0:
        return "Positivo"
    elif analise.sentiment.polarity == 0:
        return "Neutro"
    else:
        return "Negativo"

texto = "Eu adoro programar em Python!"
print(analisar_sentimento(texto))

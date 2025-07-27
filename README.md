# nathalia  from rake_nltk import Rake

def extrair_palavras_chave(texto):
    rake = Rake()
    rake.extract_keywords_from_text(texto)
    palavras_chave = rake.get_ranked_phrases()
    return palavras_chave

# Exemplo de uso:
if __name__ == "__main__":
    texto = """
    O GitHub é uma plataforma de hospedagem de código-fonte com controle de versão usando o Git. 
    Ele permite que desenvolvedores colaborem em projetos de forma eficiente.
    """
    resultado = extrair_palavras_chave(texto)
    print("Palavras-chave encontradas:")
    for palavra in resultado:
        print("-", palavra)

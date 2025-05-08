# 🧑‍💻 Portfólio Profissional – Miguel Moura

**Estudante de Engenharia de Software | CEUB**  
📍 Brasília, DF  
📧 filemoura@sempreceub.com  
🔗 [LinkedIn](https://linkedin.com/in/miguel-moura)  
💻 [GitHub](https://github.com/abraaofmedeiros/gestor_despesas_pessoais)

---

## 👨‍🎓 Perfil Pessoal

Sou Miguel, estudante de Engenharia de Software no CEUB. Me interesso por desenvolvimento de software e tecnologias inovadoras.

Tenho conhecimento em **Lua** e **Python**, e participei de cursos diversos como leilões, Airbnb, marketing digital e mercado financeiro.  
Gosto de aprender na prática, contribuir com ideias e me envolver em projetos desafiadores.

---

## 🛠️ Habilidades Técnicas

- Python  
- Lua  
- Google Workspace  
- Organização de projetos  
- Comunicação e trabalho em equipe  

---

## 💼 Projeto: Gestor de Despesas Pessoais

Projeto prático de software para controle financeiro pessoal.

**Funcionalidades:**
- Registro de despesas
- Categorização por tipo (ex: Alimentação, Transporte)
- Relatórios financeiros

**Tecnologia usada:** Python  
🔗 Repositório: [github.com/abraaofmedeiros/gestor_despesas_pessoais](https://github.com/abraaofmedeiros/gestor_despesas_pessoais)

### 🧾 Exemplo de Código:

```python
import csv

def adicionar_despesa():
    descricao = input("Descrição: ")
    valor = input("Valor: ")
    categoria = input("Categoria: ")
    with open("despesas.csv", mode="a", newline="") as arquivo:
        writer = csv.writer(arquivo)
        writer.writerow([descricao, valor, categoria])
    print("Despesa adicionada com sucesso!")

def listar_despesas():
    try:
        with open("despesas.csv", mode="r") as arquivo:
            reader = csv.reader(arquivo)
            for row in reader:
                print(f"{row[0]} - R$ {row[1]} ({row[2]})")
    except FileNotFoundError:
        print("Nenhuma despesa registrada ainda.")

if __name__ == "__main__":
    while True:
        print("\n1. Adicionar Despesa\n2. Listar Despesas\n3. Sair")
        opcao = input("Escolha: ")
        if opcao == "1":
            adicionar_despesa()
        elif opcao == "2":
            listar_despesas()
        elif opcao == "3":
            break
        else:
            print("Opção inválida.")

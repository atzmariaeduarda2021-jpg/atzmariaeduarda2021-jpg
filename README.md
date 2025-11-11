🧹 TECNODIVAS  
Limpeza com organização e inovação!

---

 🏫 Escola SESI de Ensino Médio José Pedro Fernando Piovan - São Leopoldo
Integrantes:

👩‍💻 Emily  
👩‍💻 Maria Eduarda  
👩‍💻 Milena  

---

💡 Problema
De acordo com nossa diretora Rafaela Rech, a direção enfrentava dificuldades relacionadas à limpeza do ambiente escolar.  
Observou-se que espaços da escola não estavam sendo higienizados adequadamente, e quando alguma funcionária faltava,
as demais não conseguiam cumprir toda a carga horária nem finalizar a limpeza completa dos ambientes.

---

🧭 Justificativa

Escolhemos esse problema porque a direção não tinha um controle eficiente sobre a rotina de limpeza, o que gerava sobrecarga 
e falhas na manutenção dos espaços.  
Nosso objetivo foi criar uma solução tecnológica que facilitasse o acompanhamento das funcionárias e garantisse 
um ambiente escolar sempre limpo, seguro e organizado.

---

 🎯 Objetivo

 Desenvolver e implementar um sistema digital que auxilie a diretora no controle de presença e nas atividades das colaboradoras responsáveis pela limpeza.

O sistema permite:
- Registrar quem compareceu e quem faltou;
- Calcular o tempo e o custo adicional gerado por ausências;(caso ganhasem horas extras)
- Organizar e monitorar em tempo real a higienização de salas, banheiros e áreas comuns.

Assim, garante-se eficiência, segurança e conforto para toda a comunidade escolar.

---

👩‍🔧 Quem se beneficia?

- Colaboradoras da limpeza: passam a ter um cronograma mais organizado e uma rotina de trabalho otimizada.  
- Diretora: recebe relatórios automático sobre presenças e andamento da limpeza.  
- Alunos: se beneficiam de ambientes limpos e bem cuidados, que favorecem o bem-estar e o aprendizado.

---

🔄 Fluxograma TECNODIVAS


A[Início] --> B[Login no Aplicativo]
B --> C[Registrar Presença]
C --> D[Verificar Ausências]
D -->|SIM| E[Calcular Tempo]
E --> F[Notificar Diretora]
F --> G[Organizar Higienização<br/>Salas, Banheiros e Áreas Comuns]
G --> H[Atualizar Status]
H --> I[Relatório Diário para Diretora]
D -->|NÃO| J[Registrar Atividades do Dia]
J --> K[Atualizar o Aplicativo]
I --> L[Fim]
K --> L

---
    🧰 Como será feito e utilizado
    -Serão utilizados 3 tablets Samsung Galaxy Tab A9 (64GB).
    -Instalados na secretaria e conectados ao aplicativo Tecnodivas.
    -Cada colaboradora faz o check-in diário inserindo seu código pessoal.
    -A diretora pode acompanhar em tempo real o status da higienização.
   


    📱 Valores estimados:
    | Loja          | Modelo             | Preço     |
    | ------------- | ------------------ | --------- |
    | Amazon        | Galaxy Tab A9 64GB | R$ 765,02 |
    | Mercado Livre | Galaxy Tab A9 64GB | R$ 715,00 |
    | Casas Bahia   | Galaxy Tab A9 64GB | R$ 899,00 |

---
🖥️ Programação TECNODIVAS

O sistema foi desenvolvido em Portugol, utilizando:
Tipos de dados: inteiros, reais, lógicos e textos;
Estruturas condicionais (se/senao);
Laços de repetição (para, enquanto);
Estruturas de dados (vetor e matriz);
Entradas e saídas amigáveis com menu interativo.

---

💻 Exemplo de código:
    cadeia nomes[5], status[5], continuar
    inteiro opcao
    real horasTrabalhadas[5][3], custoExtra[5]
   faca{
        escreva(":: MENU TECNODIVAS ::\n")
        escreva("1 - Registrar presença\n")
        escreva("2 - Calcular custo adicional\n")
        escreva("3 - Relatório diário\n")
        escreva("0 - Sair\n")
        leia(opcao)
        
        escolha(opcao){
            caso 1:
                escreva(":: REGISTRO DE PRESENÇA ::\n")
            pare
            caso 2:
                escreva(":: CÁLCULO DE CUSTO ::\n")
            pare
            caso 3:
                escreva(":: RELATÓRIO ::\n")
            pare
       }
    }enquanto(opcao !=0)

   ---
   💻 Nosso codigo:
      cadeia nomes[3], status[3], continuar, nomePesquisa, salas
    inteiro opcao
    real horasTrabalhadas[3][2] , custoExtra[3], totalExtra = 0, totalHoras = 0
    logico encontrada = falso

    faca {
    limpa()
      escreva("=== SISTEMA TECNODIVAS ===\n\n")
      escreva("1 - Registrar presença das colaboradoras\n")
      escreva("2 - Verificar ausências e calcular custo extra\n")
      escreva("3 - Registrar atividades de limpeza\n")
      escreva("4 - Gerar relatório diário\n")
      escreva("0 - Sair do sistema\n\n")
      escreva("Escolha uma opção: ")
       leia(opcao)

        escolha(opcao){
          caso 1:
          limpa()
            escreva(":: REGISTRO DE PRESENÇA ::\n\n")
                para(inteiro i=0; i < 3; i++){
                  escreva("Nome da colaboradora ", i + 1, ": ")
                    leia(nomes[i])
                  escreva("Ela compareceu hoje? (sim/nao): ")
                    leia(status[i]) 
                    se(status[i] == "s") {
                  escreva("Digite as horas trabalhadas nas 3 áreas (salas, banheiros, áreas comuns):\n")
                 
                para(inteiro j = 0; j < 2; j++){
                  escreva("Horas no setor ", j+1, ": ")
                    leia(horasTrabalhadas[i][j])
                } 
                    }   senao{
                   // Se faltou, define horas e custo como zero
                    para(inteiro j= 0; j < 2; j++){
                            horasTrabalhadas[i][j] = 0}
                        }   
                      escreva("\n")
                }
                escreva("Presenças registradas com sucesso!\n")
                escreva("Digite 'ENTER' para voltar ao menu...")
                leia(continuar)
          pare
          caso 2:
          limpa()
               escreva(":: VERIFICAÇÃO DE AUSÊNCIAS E CÁLCULO DE CUSTO ::\n\n")
                para(inteiro i = 0; i < 3; i++){
                    se (status[i] == "n"){
                        custoExtra[i] = 100.0   // custo fixo extra (exemplo)
                        escreva("Colaboradora ", nomes[i], " faltou. Custo adicional", custoExtra[i], "\n")
                    }
                    senao {
                        custoExtra[i] = 0
                        escreva("Colaboradora ", nomes[i], " presente. Sem custo extra.\n")
                    }
                }  

                escreva("\nVerificação concluída!\n")
                escreva("Digite ENTER para voltar ao menu...")
                leia(continuar)

          pare
          caso 3:
          limpa()
            escreva(":: REGISTRO DAS ATIVIDADES ::\n\n")
           para(inteiro i = 0; i < 3; i++){
            se(status[i] == "s"){
              escreva("- Higienização de salas concluída? (sim/nao): ")
              leia(salas)
              escreva("- Higienização de banheiros concluída? (sim/nao): ")
              leia(salas)
              escreva("- Higienização das áreas comuns concluída? (sim/nao): ")
              leia(salas)
              escreva("\nAtividades registradas!\n\n")
              
              escreva("Digite ENTER para voltar ao menu...")
          leia(continuar)

            }
            
           }
          pare
          caso 4:
          limpa()
          escreva(":: RELATÓRIO DIÁRIO ::\n\n")
          para(inteiro i = 0; i < 3; i++){
          totalHoras = horasTrabalhadas[i][0] + horasTrabalhadas[i][1]
          escreva("Colaboradora: ", nomes[i], "\n")
          escreva("Status: ", status[i], "\n")
          escreva("Total de horas trabalhadas: ", totalHoras, "\n")
          escreva("Custo adicional: R$ ", custoExtra[i], "\n\n")
          totalExtra = totalExtra + custoExtra[i]
          }
          escreva("CUSTO TOTAL EXTRA DO DIA: R$ ", totalExtra, "\n")
          escreva("Digite ENTER para voltar ao menu...")
          leia(continuar)

          pare
        }
    }enquanto(opcao != 0 )
---
🧾 Conclusão

Nosso projeto facilita e agiliza o controle da limpeza, otimizando o processo de inspeção e reduzindo falhas.
O Tecnodivas contribui para um ambiente mais organizado, confiável e eficiente, promovendo bem-estar e produtividade.

---
💜 Agradecimento

Obrigada pela atenção!
— Equipe TECNODIVAS ✨

---
📜 Licença

Este material pode ser utilizado para fins educacionais com citação da fonte
(Escola SESI de Ensino Médio José Pedro Fernando Piovan).



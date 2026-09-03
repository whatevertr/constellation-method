<p align="right"><a href="MANIFESTO.md">🇺🇸 English</a></p>

# Manifesto | Constellation Method


Eu estava no começo da minha jornada com modelos de linguagem, em tarefas do dia a dia: análise de dados, auditorias, criação de conteúdo (2025). E uma coisa me incomodava sempre: os riscos visíveis de **alucinação** e de **bajulação** (a tendência da IA a concordar com você só pra agradar). Isso tirava a previsibilidade e a confiança das entregas.

Essa dor virou curiosidade. Em vez de investigar por que a IA errava, fui atrás de **por que ela acertava**. De forma intuitiva, caí na **Engenharia de Contexto**, que eu ainda nem sei se é mesmo uma disciplina, mas concordo com a ideia de que a forma como você organiza e entrega a informação molda o comportamento do modelo. A **Tríade de Documentos** surgiu disso, antes de qualquer pesquisa formal.

 **A estrutura mudar o comportamento do modelo é uma coisa**: modelos são dirigíveis por contexto. **Se isso deixa o resultado melhor de forma significativa?** Pra mim tem funcionado, mas ou eu uso e estudo, ou eu monto um laboratório, e sou CLT, ainda não ganhei o super poder de controlar o tempo. Então trato como **hipótese**, não como fato provado, e continuo estudando.

Fui ler os porquês científicos, com o cuidado de entender melhor o comportamento dos modelos pra não reimplementar solução já descartada. Dois pontos me direcionaram nos ajustes: a bajulação **não diminui** com modelos melhores, ela cresce com a escala e com mais treino por feedback humano (Perez et al., 2022); e dar à IA um perfil seu na memória **amplifica** a concordância (até +45% no caso medido; Jain et al., CHI 2026). Aí eu entendi melhor o que eu estava tateando ao criar pisos epistêmicos, guardrails, regras: eu estava **contornando** o problema da concordância imprecisa (o sycophancy que faz errar) com contexto. Afinal, se o viés nasce nos próprios objetivos de treino, eu **escolho** não contar com o modelo se autovigiando só por instrução, e trato a conferência como **estrutura externa**. É também por isso que a Tríade **separa o Manual da Função**: o Manual personaliza, e personalização pode amplificar a concordância; as regras têm as suas taxonomias organizadas no contexto.

Minha área-mãe é a **Engenharia de Produção**, então eu olho isso com o olho de quem desenha fluxo de trabalho. Uso dois conceitos principais de lá, em português simples: **Poka-Yoke** (evitar o erro pela estrutura, não pela força de vontade, é o que a taça e o jogo da moeda fazem) e **PDCA** (melhorar checando o resultado, não só inspecionando no fim). Nada novo, estou **traduzindo** prática velha de engenharia pra um meio novo.

Tudo aqui nasce do foco em **auto-aprimoramento**, e eu uso todo dia (_dogfooding_): sou a usuária número um do meu próprio método. Documento pra aprender e contribuir, nem que seja errando. 

🍷 Estava organizando uns processos... 

---
*Documento vivo. A trilha de commits deste repositório é o registro datado da sua evolução.*

# FAQ – Transporte Escolar (levantamento a partir dos áudios e das conversas de WhatsApp do CECATE)

**Fontes:**
1. **Áudios avulsos:** 13 áudios de WhatsApp (`dados/*.opus`, abr–ago/2026), transcritos automaticamente (Whisper *medium*) em `dados/transcricoes/`. Desses, 12 têm conteúdo; `PTT-20260617-WA0058` não tem fala reconhecível (verificar manualmente).
2. **Conversas de atendimento do CECATE:** 30 exportações de WhatsApp (`dados/Conversas WhatsApp CECATE/*.zip`, 23/03 a 28/04/2026). São 29 conversas distintas, porque `+55 41 3608-7607` está duplicada. Os 17 áudios de dentro das conversas foram transcritos (Whisper *medium*) e estão em `dados/transcricoes/conversas/`. As capturas de tela de erro foram lidas para registrar as mensagens exatas.
   - **Aproveitadas:** 26 conversas.
   - **Descartadas:** `62 9162-5788` (mensagem fora do escopo, de uma vidraçaria), `41 3608-7607` (só a identificação, sem dúvida registrada) e `64 8119-1981` (dúvida só em mídia não exportada).

> Termos corrigidos na leitura da transcrição: "Bebê Gestão Ágil" → **BB Gestão Ágil**; "mata burso" → **mata-burro**; "sistema 7" / "SETI" → **SETE**; "Pereira, Holândia" → **Perolândia/GO**. "Equilóquio" (WA0026) e "Redline" (WA0067) não foram identificados; conferir no áudio.
>
> Na seção 7.2, a usuária de Perolândia/GO confundiu o SETE com outro sistema (é esse outro que exige a "unidade consumidora"). A resposta do CECATE sobre o SETE continua válida.

---

## Resumo por tema

| # | Tema | Áudios | Conversas | Total |
|---|------|:---:|:---:|:---:|
| 1 | SETE – acesso e gestão de usuários (Habilita+, gov.br, trocar responsável) | – | 8 | 8 |
| 2 | SETE – erros de login, instabilidade e versão desktop | – | 7 | 7 |
| 3 | SETE – cadastro de motoristas e monitores (erro ao salvar, CPF já existe) | – | 7 | 7 |
| 4 | SETE – rotas: traçado, georreferenciamento e turnos | 3 | 1 | 4 |
| 5 | Capacitações do CECATE (inscrição, datas, horário) | – | 4 | 4 |
| 6 | SETE – relatórios e impressão (alunos por rota, mapa em PDF) | 3 | – | 3 |
| 7 | Cadastro de alunos (quem cadastrar, endereço, atualização) | 1 | 2 | 3 |
| 8 | Aluno que mora em outro município / rota na divisa | 2 | – | 2 |
| 9 | Acesso ao SIGECON (FNDE) | 2 | – | 2 |
| 10 | Demandas ao FNDE por ofício (valores do PNATE, alterações no sistema) | – | 2 | 2 |
| 11 | PNATE – prestação de contas no BB Gestão Ágil | 1 | – | 1 |
| 12 | Regulamentação municipal do transporte escolar | 1 | – | 1 |
| 13 | Uso dos veículos para universitários / outros públicos | 1 | – | 1 |
| 14 | Canais de suporte (qual WhatsApp regional procurar) | – | 1 | 1 |

*Uma conversa pode tratar de mais de um tema (por exemplo, Alfenas/MG aparece nos temas 2, 3 e 7), por isso a soma da coluna passa de 26.*

**O que muda com as conversas:** o tema mais frequente deixa de ser a operação das rotas e passa a ser o **acesso ao SETE e a gestão de usuários**. Somado aos erros de login e ao cadastro de motoristas e monitores, isso responde por 22 das 32 citações de tema nas conversas. São dúvidas objetivas e repetitivas, boas candidatas a respostas automáticas no chatbot.

**Padrão do atendimento:** em quase todo caso técnico, o CECATE pede (1) nome, município e tipo de vínculo (gestor municipal ou CACS) e (2) prints de todas as abas preenchidas ou um vídeo do erro. O chatbot pode pedir essas informações logo no início, antes de passar o caso para o atendimento humano.

---

## Perguntas frequentes

### 1. SETE – Acesso e gestão de usuários

**1.1 Preciso de acesso ao SETE, mas o responsável anterior saiu da prefeitura e ninguém tem a senha. O que faço?**
*Origem: Paranavaí/PR, Santo Antônio do Palma/RS, Buriti Alegre/GO, município do PA (94 8401-8469).*
*Resposta (dada pelo CECATE):* agora o cadastro no SETE começa pelo(a) **secretário(a) de Educação**, que deve se cadastrar no **Habilita+** (tutorial: https://www.gov.br/fnde/pt-br/assuntos/sistemas/habilita). Com esse cadastro, o secretário passa a ter perfil de **administrador** no SETE e pode incluir e remover os demais usuários. O acesso por e-mail está sendo retirado aos poucos; no futuro, o login será feito só pelo **gov.br**.

**1.2 Ao me registrar, aparece "O EMAIL INFORMADO JÁ EXISTE. VERIFIQUE E TENTE NOVAMENTE!". Por quê?**
*Origem: Paranavaí/PR.*
*Resposta:* esse e-mail (em geral o institucional da secretaria) já está vinculado a outro usuário, normalmente o responsável anterior. O secretário, com acesso pelo Habilita+, confere quem está cadastrado com esse e-mail e remove ou ajusta o usuário.

**1.3 Como trocar o coordenador ou excluir o usuário de quem saiu? O responsável pode ser um contratado?**
*Origem: município do PA (94 8401-8469), Buriti Alegre/GO.*
*Resposta:*
- Na lista de usuários, quem é **Admin** exclui clicando no ícone **X** da coluna "Ações" e inclui com "Adicionar um novo usuário". O CECATE indicou um vídeo para a inclusão: https://youtu.be/D_NNaSZYxVY
- O papel **Editor** não permite alterar usuários. Se o secretário estiver como Editor, é preciso pedir à **CMATE/FNDE** (cmate@fnde.gov.br) que mude o papel para Admin.
- **Sim**, o responsável pode ser uma pessoa contratada.

**1.4 Aparece "ERRO AO REMOVER O USUÁRIO", mesmo depois de desativar o usuário ou mudar o papel dele.**
*Origem: Gentil/RS.*
*Resposta:* primeiro tentar reativar o usuário e excluir; depois, mudar o papel para Leitor ou Editor e tentar de novo. Se o erro continuar, gravar um vídeo com o passo a passo e enviá-lo ao CECATE junto com o e-mail vinculado, para que o caso seja passado à equipe técnica. Trata-se de uma falha do sistema, não de um erro de uso.

**1.5 Cadastrei meu e-mail pessoal (Gmail) em vez do institucional. Como corrijo, se ainda não existe nenhum gestor cadastrado?**
*Origem: 44 8417-6177.*
*Resposta-base:* um usuário Admin pode editar o e-mail em "edição de usuários". Se não houver Admin, o secretário de Educação se cadastra no Habilita+ (ver 1.1) e faz a correção. **Lacuna:** a conversa terminou sem solução; confirmar esse caminho.

**1.6 Posso entrar no SETE com o login gov.br do secretário?**
*Origem: 64 8103-5684.*
*Resposta (dada pelo CECATE):* **não é recomendado**. Cada pessoa precisa ter o próprio login, e o secretário (Admin) deve cadastrar o seu usuário. Se o sistema mostrar dados de outra pessoa ou travar no login: limpar o histórico, o cache e os cookies do navegador, entrar de novo e, se preciso, testar outro navegador (o CECATE sugeriu o Edge).

**1.7 Fiz o registro no SETE, ele ficou "em análise" e não tive retorno. Como recupero o acesso?**
*Origem: 66 9204-2256.*
*Resposta-base:* o novo usuário precisa ser liberado pelo Admin do município (o secretário, via Habilita+). Pedir a liberação a ele. **Lacuna:** a conversa não chegou a uma resposta; confirmar quem analisa esses registros e em quanto tempo.

### 2. SETE – Erros de login, instabilidade e versão desktop

**2.1 No SETE desktop, ao entrar pelo gov.br, aparece "UNEXPECTED TOKEN 'E', "EYJPZF91C3"... IS NOT VALID JSON". O que fazer?**
*Origem: 51 9364-9072, Canguçu/RS, 94 8402-2157.*
*Resposta (dada pelo CECATE):* instalar a **versão mais recente** do SETE desktop (em 10/04/2026 era a **5.1.0**; a 5.0.0 apresentava o erro), baixada da página do FNDE: https://www.gov.br/fnde/pt-br/acesso-a-informacao/acoes-e-programas/programas/pnate/sete-sistema-eletronico-de-gestao-do-transporte-escolar-versao-desktop
*Manutenção:* manter no chatbot o número da versão atual.

**2.2 Aparece "ACESSO INVÁLIDO" ou não consigo entrar no sistema.**
*Origem: Alfenas/MG, São Simão/GO, 64 8103-5684 (todas em 07/04/2026).*
*Resposta:* tentar pela **versão web**, com login **gov.br**. Se não funcionar, pode ser uma instabilidade geral: em 07/04/2026, o CECATE informou a vários municípios que havia instabilidade e que a equipe estava trabalhando na solução. **Lacuna:** um aviso de status ou instabilidade que o chatbot possa consultar e informar.

**2.3 Devo usar o SETE web ou o desktop?**
*Origem: Alfenas/MG.* A usuária sempre usou o aplicativo instalado no notebook e nunca tinha tentado pelo gov.br.
*Resposta:* o CECATE orienta usar a **versão web com gov.br**. Se usar o desktop, manter a versão atualizada (ver 2.1).

**2.4 A tela abre, mas não aceita digitação, ou o sistema não carrega.**
*Origem: Perolândia/GO.*
*Resposta:* verificar a conexão com a internet (no caso relatado, a internet estava ruim) e enviar ao CECATE um vídeo mostrando o problema.

### 3. SETE – Cadastro de motoristas e monitores

**3.1 Aparece "ERRO AO SALVAR O MOTORISTA", ou o monitor simplesmente não é salvo. O que fazer?**
*Origem: Igrejinha/RS, Redenção/PA, Mateiros/TO, Humaitá/RS.*
*Resposta (dada pelo CECATE):*
1. Vincular o motorista ou monitor a **pelo menos uma rota** e tentar salvar de novo.
2. Verificar se o profissional **já trabalhou como motorista em outro município** e se já foi cadastrado no SETE lá (ver 3.2).
3. Se o erro continuar, enviar ao CECATE prints de **todas as abas preenchidas** (Dados pessoais e Dados de transporte).

**3.2 Aparece "O CPF INFORMADO JÁ EXISTE" (às vezes com "MUNICÍPIO: …"). Como cadastrar?**
*Origem: Humaitá/RS (CPF já cadastrado em Sede Nova/RS), Guidoval/MG (monitor), Siderópolis/SC (servidor que ainda consta em Treviso/SC).*
*Resposta:* o profissional está cadastrado em outro município. Pedir à **prefeitura anterior** que o remova. Se ele trabalha nos dois municípios ao mesmo tempo, o CECATE encaminha o caso à equipe técnica ou à **CMATE/FNDE**. Quando a mensagem não informa município, conferir também se o CPF já está cadastrado (mesmo inativo) no próprio município.
**Lacuna:** falta uma regra oficial para profissionais que atuam em mais de um município. No caso de Humaitá/RS, a solução levou mais de duas semanas.

**3.3 O erro ao confirmar o condutor aparece só às vezes e some depois de uns 30 minutos. É normal?**
*Origem: Humaitá/RS.*
*Resposta:* é instabilidade do sistema. Tentar novamente mais tarde e, se o erro persistir, enviar prints dos dados.

**3.4 Aparece uma mensagem técnica como "ERRO AO SALVAR O MONITOR. FALHA AO INSERIR O REGISTRO… COLUMN "CRIADO_POR" … DOES NOT EXIST".**
*Origem: Alfenas/MG (08/04/2026).*
*Resposta:* é uma falha interna do sistema, que o usuário não consegue resolver. Enviar o print ao CECATE. No caso relatado, o cadastro voltou a funcionar dois dias depois.

### 4. SETE – Rotas: traçado, georreferenciamento e turnos

**4.1 Como alterar ou estender uma rota já cadastrada (incluir novos pontos) sem refazer tudo?**
*Origem: 20260616-WA0015.* A rota é longa, rural e na divisa; entraram dois novos pontos. A usuária soube que dá para fazer em "Desenhar rotas", mas não conseguiu pelos ícones e pede um vídeo.
*Resposta-base:* editar o traçado existente na ferramenta de desenho de rotas do SETE, acrescentando os novos pontos. **Lacuna:** indicar um tutorial oficial.

**4.2 Como levantar as coordenadas dos pontos de embarque dos alunos?**
*Origem: 20260510-WA0054, 20260510-WA0073 (respostas de colegas – boas práticas); Perolândia/GO.*
- Percorrer a rota junto com o motorista, marcando cada ponto de embarque, quantos e quais alunos embarcam em cada um e as coordenadas.
- Ou o motorista envia a coordenada (pelo celular) no momento do embarque, e o técnico lança no sistema.
- Os pais também podem enviar as coordenadas da casa do aluno para georreferenciá-lo (orientação do CECATE).
- Registrar também os obstáculos da via (pontes, mata-burros etc.) e medir a quilometragem real.
- O motorista é o "ponto focal" em campo, e o técnico é quem alimenta o SETE.

**4.3 A mesma rota é feita de manhã, à tarde e à noite. Cadastro uma rota por turno? E que quilometragem informo?**
*Origem: Humaitá/RS.*
*Resposta (dada pelo CECATE):* cadastrar **uma rota só** e marcar os turnos em que ela é feita. A quilometragem é a de **um percurso**, não o total do dia (ex.: 75 km por dia em 3 turnos → informar **25 km**).
**Validar:** o município não tem turno noturno e mesmo assim foi orientado a marcar as três opções; confirmar se o correto é marcar só os turnos em que a rota realmente opera.

### 5. Capacitações do CECATE

**5.1 O CECATE oferece capacitação no SETE? Como fico sabendo?**
*Origem: Santo Antônio de Posse/SP.*
*Resposta:* sim. As capacitações são divulgadas no site **https://cecate.fct.ufg.br/**.

**5.2 A capacitação tem dois dias. Preciso ir nos dois?**
*Origem: Gouvelândia/GO, Paranaíba/MS.*
*Resposta:* **não**. Cada município participa em **um dia específico**, informado no site (ex.: capacitação de Jataí: https://cecate.fct.ufg.br/p/60175-14-capacitacao-jatai). A regra vale tanto para **gestores** quanto para **CACS**.

**5.3 Que horas a capacitação termina?**
*Origem: Paranaíba/MS.*
*Resposta:* na capacitação de Jataí (29–30/04/2026), **até as 18h**, conforme o site. Terminada a programação do seu dia, o participante está liberado.

**5.4 Não consigo concluir a inscrição (o formulário não aceita o telefone).**
*Origem: 64 9976-5379.*
*Resposta:* informar o celular com o **9 inicial** e **sem espaço** entre o DDD entre parênteses e o número, por exemplo: `(64)99999-9999`.

### 6. SETE – Relatórios e impressão

**6.1 Como imprimir a lista de alunos de cada rota, separada por rota, com nome e quantidade?**
*Origem: WA0050, WA0079.* A usuária relata que, pelo menu de Rotas, não conseguia copiar/colar nem imprimir a lista completa; resolveu com orientação de um colega (Marcos) por outro caminho.
*Resposta-base (validar no SETE):* usar o módulo de relatórios/listagem de alunos filtrando pela rota e exportar (PDF/planilha), em vez de copiar da tela de detalhes da rota.

**6.2 Como gerar o mapa da rota em PDF para enviar à prefeitura?**
*Origem: WA0099.*
*Resposta-base (validar no SETE):* abrir a rota no mapa e usar a opção de exportar/imprimir do módulo de rotas. **Lacuna:** falta um passo a passo oficial ou tutorial em vídeo.

### 7. Cadastro de alunos

**7.1 No SETE, cadastro só os alunos da rede municipal?**
*Origem: Alfenas/MG.*
*Resposta (dada pelo CECATE):* **não**. Devem ser cadastrados **todos os alunos que usam o transporte escolar**: das redes municipal, estadual e federal.

**7.2 Onde cadastro o aluno? E se a família não tiver comprovante de endereço (conta de energia com a "unidade consumidora")?**
*Origem: Perolândia/GO.*
*Resposta (dada pelo CECATE):* pelo menu lateral **Alunos → Cadastrar**. O SETE **não exige unidade consumidora**, e o endereço é **opcional**. Para localizar o aluno no mapa, peça aos pais as **coordenadas** da residência (ver 4.2).

**7.3 Como manter o cadastro de alunos do transporte sempre atualizado?**
*Origem: 20260510-WA0073 (boa prática relatada).*
- Na matrícula, a escola já envia a ficha do aluno com a **linha que ele vai usar**.
- Quando há transferência, a escola avisa imediatamente, e o técnico dá baixa no SETE e no sistema estadual, se houver.
- Sem o fluxo **escola → técnico → motorista**, o sistema fica desatualizado e os dados enviados ao Estado e à União ficam errados.

### 8. Aluno de outro município / residência na divisa

**8.1 O aluno está matriculado no meu município, mas mora (ou o endereço aparece no mapa) em outro município, perto da divisa. Posso transportá-lo? Tem problema?**
*Origem: 20260507-WA0026, citado também em 20260616-WA0015.*
*Resposta-base (validar com o FNDE):* o que vale para o programa é a **matrícula na rede** (Censo Escolar) e o uso do transporte escolar público. O atendimento de alunos que moram na divisa é comum e recomenda-se formalizar com o município vizinho (convênio ou termo de cooperação) e registrar corretamente o endereço no SETE.

### 9. Acesso ao SIGECON (FNDE)

**9.1 O SIGECON está com problema ou sem acesso. Outros municípios também estão com problema?**
*Origem: 20260429-WA0041, 20260429-WA0067.* Relato de que a instabilidade foi reconhecida na capacitação do SETE; o último lançamento feito foi de 2022, e a equipe não consegue acessar.
*Resposta-base:* verificar os perfis e credenciais de acesso (gestor/cadastrador) e abrir chamado nos canais do FNDE. **Lacuna:** incluir no FAQ o canal oficial de suporte e o procedimento de recuperação de acesso.

### 10. Demandas ao FNDE por ofício

**10.1 O valor do PNATE que recebemos veio menor que o esperado. A quem pergunto?**
*Origem: Paranhos/MS (repasse de 01/04/2026).*
*Resposta (dada pelo CECATE):* o CECATE não responde por valores. Enviar um **ofício ao FNDE**, que gere os recursos do PNATE, com as dúvidas e os questionamentos.

**10.2 Quero pedir uma mudança ou tratamento específico no SETE. Como faço?**
*Origem: Juína/MT.*
*Resposta (dada pelo CECATE):* enviar um **ofício ao FNDE** (desenvolvedor do sistema) com a **justificativa técnica e legal** do pedido.

**Contato para os ofícios (informado pelo CECATE):** Coordenação de Monitoramento, Avaliação e Apoio à Gestão do Transporte Escolar – **CMATE/FNDE** · SBS Q. 2, Asa Sul, Brasília-DF, 70655-775 · (61) 2022-5111 · cmate@fnde.gov.br

### 11. PNATE – Prestação de contas (BB Gestão Ágil)

**11.1 No BB Gestão Ágil, ao informar a chave de acesso da nota fiscal, o campo "valor do documento" fica zerado e não pode ser editado. Isso vai gerar problema na prestação de contas?**
*Origem: 20260623-WA0023.*
*Resposta-base:* registrar evidências (prints), guardar as notas fiscais e comunicar o problema ao Banco do Brasil e ao FNDE. **Lacuna:** confirmar com o FNDE se existe orientação oficial sobre esse erro.

### 12. Regulamentação municipal

**12.1 Existe um modelo de regulamentação municipal do transporte escolar? Por onde começar?**
*Origem: 20260506-WA0128.*
*Resposta-base:* montar uma norma municipal (lei, decreto ou portaria) que trate de quem tem direito, distância mínima, rotas, pontos de embarque, monitores, obrigações do motorista e do veículo (CTB arts. 136–139, vistoria, curso específico), uso dos veículos, fiscalização e controle social. **Lacuna:** reunir modelos de outros municípios para oferecer como anexo.

### 13. Uso dos veículos e público atendido

**13.1 Os ônibus do transporte escolar (Caminho da Escola / cedidos pelo Estado) podem transportar universitários ou atender outras secretarias?**
*Origem: 20260507-WA0076.* No município citado, os universitários são atendidos pela Assistência Social, com veículo e motorista próprios, porque os ônibus cedidos são só para alunos da zona rural.
*Resposta-base:* os veículos do Caminho da Escola e os recursos do PNATE são destinados aos **alunos da educação básica pública**, prioritariamente os da zona rural. Transportar universitários deve ser feito com outros recursos e veículos, conforme a lei municipal. Checar os termos de doação/cessão do veículo.

### 14. Canais de suporte

**14.1 Qual WhatsApp de suporte do SETE devo procurar?**
*Origem: Guidoval/MG (entrou em contato com a região errada). Os números aparecem em todas as mensagens de erro do SETE.*
- Região **Centro-Oeste, Norte e Sul:** +55 62 3209-6723 (CECATE/UFG)
- Região **Nordeste:** +55 77 9199-1990
- Região **Sudeste:** +55 34 8407-7958

Ao entrar em contato, informar o nome completo, o município e o tipo de vínculo (gestor municipal ou CACS) e enviar prints ou um vídeo do erro.

---

## Lacunas para o chatbot (conteúdo a produzir)
1. Passo a passo (texto + vídeo) do SETE para: imprimir alunos por rota, exportar o mapa da rota em PDF e editar ou estender uma rota.
2. Canal oficial de suporte do FNDE para o SIGECON e procedimento de recuperação de acesso.
3. Posição oficial sobre o "valor do documento zerado" no BB Gestão Ágil.
4. Modelo de regulamentação municipal do transporte escolar.
5. Orientação formal sobre alunos residentes em outro município.
6. Passo a passo do **Habilita+ → SETE** (secretário vira Admin → cadastra usuários), incluindo: o que fazer quando o secretário está como Editor, quando o e-mail já existe e quando o cadastro foi feito com e-mail pessoal.
7. Regra e fluxo para **CPF de motorista ou monitor já cadastrado em outro município**, inclusive para quem trabalha em dois municípios.
8. Forma de o chatbot saber de **instabilidades** em andamento e da **versão atual** do SETE desktop.
9. Confirmar a regra de **turnos na rota** (marcar só os turnos em que a rota opera ou todos) e da quilometragem por percurso.
10. Quem analisa os registros "em análise" no SETE e em quanto tempo.

---

## Anexo – Conversas do CECATE por tema

| Arquivo (`Conversa do WhatsApp com +55 …`) | Município | Temas |
|---|---|---|
| 19 93300-4500 | Santo Antônio de Posse/SP | 5.1 |
| 32 8425-3508 | Guidoval/MG | 3.2, 14.1 |
| 35 9816-5687 | Alfenas/MG | 2.2, 2.3, 3.4, 7.1 |
| 44 8417-6177 | não informado | 1.5 |
| 44 9903-3838 | Paranavaí/PR | 1.1, 1.2 |
| 48 9834-0230 | Siderópolis/SC | 3.2 |
| 51 9315-5417 | Igrejinha/RS | 3.1 |
| 51 9364-9072 | não informado | 2.1 |
| 53 8158-5772 | Canguçu/RS | 2.1 |
| 54 9625-6450 | Santo Antônio do Palma/RS | 1.1 |
| 54 9683-5491 | Gentil/RS | 1.4 |
| 55 9718-2526 | Humaitá/RS | 3.1, 3.2, 3.3, 4.3 |
| 62 8603-4910 | São Simão/GO | 2.2 |
| 63 9245-8809 | Mateiros/TO | 3.1 |
| 64 8103-5684 | não informado | 1.6, 2.2 |
| 64 8435-8764 | Buriti Alegre/GO | 1.1, 1.3 |
| 64 9318-3209 | Perolândia/GO | 2.4, 4.2, 7.2 |
| 64 9324-9010 | Gouvelândia/GO | 5.2 |
| 64 9976-5379 | não informado | 5.4 |
| 66 9204-2256 | não informado | 1.7 |
| 66 9255-0968 | Juína/MT | 10.2 |
| 67 8434-4615 | Paranaíba/MS | 5.2, 5.3 |
| 67 9653-5397 | Paranhos/MS | 10.1 |
| 94 8401-8469 | não informado (PA) | 1.1, 1.3 |
| 94 8402-2157 | não informado | 2.1 |
| 94 9154-0285 | Redenção/PA | 3.1 |

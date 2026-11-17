# Plano de implementação

## Escopo

Construir um site estático multipágina, em português do Brasil, para o portal **Conserto e manutenção de portões eletrônicos em Ribeirão Preto**. O site capta contatos via WhatsApp e telefone e registra cliques no endpoint Google Apps Script fornecido. O portal não se apresenta como executor direto do serviço. Não publicar o site nesta tarefa.

O projeto terá 13 documentos HTML reais: página inicial; 3 páginas de serviço; páginas dos bairros Centro, Jardim Botânico, Nova Aliança, Vila Tibério, Bonfim Paulista e Campos Elíseos; Sobre; Perguntas frequentes; Política de privacidade. Incluir imagens, um CSS, um tracker JS, um arquivo config JS centralizado, favicon, sitemap, robots, llms.txt, Code.gs, documentação e configuração Vercel.

## Implementação

- HTML, CSS e JavaScript nativos, sem bibliotecas de frontend ou dependências npm. Manter conteúdo principal e metadados no HTML de cada página. Navegação por URLs limpas com `index.html` dentro de pastas.
- Estrutura: `index.html`, `servicos/<slug>/index.html`, `bairros/<slug>/index.html`, `sobre/index.html`, `perguntas-frequentes/index.html`, `politica-de-privacidade/index.html`, `img/`, `style.css`, `tracker.js`, `config.js`, `favicon.svg`, `sitemap.xml`, `robots.txt`, `llms.txt`, `vercel.json`, `apps-script/Code.gs`, `LEIA-ME.txt`, `TODO.md`, `plan.md`, `manus-routes.json`, `app.config.ts`, `.gitignore`, `package.json` sem dependências e `build.js` nativo.
- Usar o slug `portaoeletronicoribeiraopreto` como site/domínio-base e `https://portaoeletronicoribeiraopreto.vercel.app` como origin canônico inicial, facilmente trocável no LEIA-ME.
- Escolher três serviços reais: conserto de motor de portão eletrônico; manutenção preventiva e ajuste de portão eletrônico; instalação de automatizador para portão. Criar conteúdo útil, exclusivo e não repetitivo, com no mínimo 250 palavras por página de serviço e 150 por página de bairro.
- Em conteúdo de segurança elétrica, orientar cautela, não instruir reparos em fiação energizada e recomendar confirmar escopo e condições com o prestador ou fabricante. Não afirmar leis, certificações ou requisitos sem fonte.
- Centralizar números, nicho, cidade, mensagem padrão e endpoint em `config.js`. Reproduzir sem alteração da lógica o tracker do Anexo A e copiar o Apps Script do Anexo B do arquivo anexado. Cada link de contato terá os atributos de rastreamento e valores provisórios pedidos.
- Gerar 5 fotos ilustrativas: `hero.jpg` horizontal 16:9, `sobre.jpg` e uma foto por serviço 4:3. Manter aspecto de foto cotidiana realista, sem texto, logos, rostos em destaque ou elementos publicitários; otimizar imagens para web e usar alt neutro.
- Aplicar SEO e GEO em cada página: HTML inicial completo, title e meta description dentro dos limites, canonical, Open Graph e Twitter, JSON-LD apropriado, hierarquia de títulos, links internos, breadcrumbs nas páginas internas, sitemap com 13 URLs, robots e `llms.txt`. O `Organization` do `Service` identifica o portal como contato e deixa explícito que ele encaminha pedidos, sem executar diretamente o serviço. Garantir respostas FAQ consistentes entre HTML e JSON-LD.
- Incluir aviso legal exato em todo rodapé e política de privacidade compatível com os dados de eventos descritos, sem coleta de nome, e-mail ou CPF e sem cookies publicitários.
- Implementar o layout responsivo baseado na referência fornecida: navegação em pílula, hero com foto e overlay, formulário rápido sobreposto, seções creme e lavanda, cartões arredondados, CTAs WhatsApp/telefone, barra fixa mobile, foco visível, contraste AA, alvos de toque de pelo menos 44 px e `prefers-reduced-motion`.
- Configurar `package.json` sem dependências, `build.js` nativo exatamente como fornecido e `vercel.json` com build `npm run build`, saída `dist`, `cleanUrls` e `trailingSlash`. Um script `postbuild` nativo remove de `dist` os documentos de projeto, manifesto de rotas e metadado de identidade para que não sejam publicados como páginas; `.gitignore` exclui `dist/` e `node_modules/`.
- Definir o logo do projeto WebDev via `app.config.ts` com uma URL HTTPS durável do favicon próprio, sem alterar o favicon usado pelo site.
- Documentar no LEIA-ME a importação na Vercel como site estático e as tarefas manuais do Google Apps Script, Search Console e Perfil da Empresa no Google.

## Direção visual

- **Movimento de design:** landing page local acolhedora e orgânica, conforme a referência visual fornecida pelo usuário.
- **Princípios:** leitura direta; confiança sem alegações promocionais; fotografias contextuais discretas; interações de contato evidentes e acessíveis.
- **Filosofia de cor:** lavanda e violeta profundo associam-se ao tema técnico sem parecer agressivos. Fundo creme e superfícies suaves preservam acolhimento; verde fica reservado ao botão do WhatsApp; telefone em tom escuro.
- **Layout:** hero amplo com bordas arredondadas, formulário rápido parcialmente sobreposto e seções de conteúdo em largura confortável. Cartões de serviço em desktop tornam-se pilha legível no celular.
- **Elementos marcantes:** barra branca flutuante em pílula; selo local translúcido no hero; destaque lavanda na busca rápida e nos cartões.
- **Interação:** links de WhatsApp e telefone visíveis, com mensagem de serviço/bairro quando pertinente; formulário rápido compõe a mensagem a partir das escolhas; navegação por teclado com estado de foco evidente.
- **Animação:** transições discretas, sem dependência de animação para revelar conteúdo; respeitar `prefers-reduced-motion`.
- **Tipografia:** Fira Sans em Google Fonts com fallback de sistema; títulos compactos e legíveis, corpo confortável.
- **Essência da marca:** portal de contato local para quem precisa encaminhar um pedido de conserto ou manutenção de portões eletrônicos em Ribeirão Preto; personalidade direta, cuidadosa e acessível.
- **Violeta de destaque:** `#4C1D95`; escura (mistura com 28% de preto) `#37156B`; suave (mistura com 92% de branco) `#F1EDF7`; suave 2 (mistura com 80% de branco) `#DBD2EA`.

# Site Wiztech Automação

Site de uma página, estático (HTML/CSS/JS puro). Não precisa de servidor nem de banco de dados.
Hospedagem prevista: GitHub Pages (grátis) + domínio .com.br no Registro.br.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | O site inteiro |
| `logo-icone.svg` | Ícone da logo (fundo claro) |
| `logo-icone-escuro.svg` | Ícone da logo (fundo escuro, usado no rodapé) |
| `favicon.svg` | Ícone da aba do navegador |
| `og-image.png` | Imagem que aparece ao compartilhar o link (WhatsApp, LinkedIn) |
| `robots.txt` / `sitemap.xml` | Ajudam o Google a encontrar o site |

## Checklist — quando o CNPJ sair

### Dados para trocar no `index.html`

- [ ] **WhatsApp** — linha `const WHATSAPP = '5571900000000';` (perto do fim). Formato: 55 + DDD + número, só dígitos.
- [ ] **CNPJ** — rodapé: `CNPJ 00.000.000/0001-00`
- [ ] **CREA** — seção Sobre: `CREA-BA nº [00000]`
- [ ] **E-mail** — seção Contato: `contato@wiztech.com.br` (aparece 2 vezes na mesma linha)
- [ ] **Endereço do site** — topo do arquivo, linhas `og:url` e `og:image`
- [ ] **Foto** (opcional) — seção Sobre, bloco "Sua foto aqui" (instrução em comentário no código)

### Outros arquivos

- [ ] `robots.txt` e `sitemap.xml` — conferir se o domínio está certo (`www.wiztech.com.br`)

### Publicação

1. [ ] Registrar o domínio no registro.br com o CNPJ
2. [ ] GitHub: Settings → Pages → Source: `main` / root
3. [ ] GitHub: Settings → Pages → Custom domain: `www.wiztech.com.br` (cria o arquivo `CNAME` sozinho)
4. [ ] Registro.br → domínio → DNS → "Editar zona" e criar:

   | Tipo | Nome | Valor |
   |---|---|---|
   | A | (vazio / @) | 185.199.108.153 |
   | A | (vazio / @) | 185.199.109.153 |
   | A | (vazio / @) | 185.199.110.153 |
   | A | (vazio / @) | 185.199.111.153 |
   | CNAME | www | SEU-USUARIO.github.io |

5. [ ] Esperar o DNS propagar (de minutos a algumas horas) e marcar **Enforce HTTPS** no GitHub Pages
6. [ ] Testar: abrir o site no celular, enviar o formulário, compartilhar o link no WhatsApp e ver a prévia
7. [ ] Cadastrar no Google Search Console e enviar o `sitemap.xml`
8. [ ] Criar o Perfil da Empresa no Google (Google Meu Negócio)

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

- [x] **WhatsApp** — linha `const WHATSAPP = '5571991132719';` (perto do fim). Formato: 55 + DDD + número, só dígitos.
- [x] **CNPJ** — rodapé: `CNPJ 00.000.000/0001-00`
- [x] **CREA** — seção Sobre: `CREA-BA nº [00000]`
- [x] **E-mail** — seção Contato: `contato@wiztechautomacao.com.br` (aparece 2 vezes na mesma linha)
- [x] **Endereço do site** — topo do arquivo, linhas `og:url` e `og:image`
- [x] **Foto** — removida da seção Sobre (sem trabalhos realizados ainda)

### Outros arquivos

- [x] `robots.txt` e `sitemap.xml` — conferir se o domínio está certo (`www.wiztechautomacao.com.br`)

### Publicação

1. [x] Registrar o domínio no registro.br
2. [ ] GitHub: Settings → Pages → Source: `main` / root
3. [x] Arquivo `CNAME` com `www.wiztechautomacao.com.br` já está no repositório
4. [ ] Registro.br → domínio → DNS → "Editar zona" e criar:

   | Tipo | Nome | Valor |
   |---|---|---|
   | A | (vazio / @) | 185.199.108.153 |
   | A | (vazio / @) | 185.199.109.153 |
   | A | (vazio / @) | 185.199.110.153 |
   | A | (vazio / @) | 185.199.111.153 |
   | CNAME | www | alissoncraig.github.io |

5. [ ] Esperar o DNS propagar (de minutos a algumas horas) e marcar **Enforce HTTPS** no GitHub Pages
6. [ ] Testar: abrir o site no celular, enviar o formulário, compartilhar o link no WhatsApp e ver a prévia
7. [ ] Cadastrar no Google Search Console e enviar o `sitemap.xml`
8. [ ] Criar o Perfil da Empresa no Google (Google Meu Negócio)

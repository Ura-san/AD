# Plataforma B2B de Fornecimento

Projeto inicial preparado para desenvolvimento com **Supabase** e deployment em **Vercel**.

## O que já está pronto

- Next.js com TypeScript
- Configuração básica de Supabase
- Estrutura inicial de página e CSS global
- `package.json` com scripts de desenvolvimento
- `.env.example` para variáveis de ambiente
- `vercel.json` para implantação organizada

## Configurar localmente

1. Instale o Node.js 20.x e npm localmente. Este workspace usa `.nvmrc` / `.node-version` para definir a versão recomendada.

2. Instale dependências:

```bash
npm install
```

3. Crie um projeto no Supabase e copie:
   - `SUPABASE_URL`
   - `SUPABASE_ANON_KEY`

3. Crie um arquivo `.env.local` com estes valores:

```env
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
```

4. Inicie o servidor de desenvolvimento:

```bash
npm run dev
```

## Usar no Vercel

No painel do Vercel, configure as mesmas variáveis de ambiente:

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`

Depois, conecte o repositório e faça deploy.

## Como usar este projeto

- `app/page.tsx` já faz uma tentativa de consulta na tabela `fornecedores`
- Crie a tabela `fornecedores` no Supabase com colunas como `id` e `nome`
- Expanda com rotas, autenticação e páginas de cadastro B2B

## Recomendações iniciais

- Use Supabase Auth para controle de clientes e fornecedores
- Defina políticas RLS para garantir segurança dos dados
- Crie APIs server-side com `app/api` para integração B2B

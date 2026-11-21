# Painel Operacional · Expedição (Netlify + Supabase)

Todos com o link veem o painel. Só quem sabe a senha de editor atualiza os dados.

## 3 passos

1. **Supabase** (supabase.com): crie um projeto. Em *SQL Editor* → *New query*, cole o conteúdo de `supabase.sql`.
   Antes de rodar, troque `TROQUE_ESTA_SENHA` pela senha dos editores **somente na linha marcada com `TROQUE A SENHA AQUI`**. Não mexa no resto. Depois clique em *Run*.
2. **Chaves:** em *Project Settings* → *API*, copie a **Project URL** e a chave **anon public**.
   Cole no começo do `index.html` (ou me envie que eu preencho). Nunca use a chave `service_role`.
3. **Netlify** (app.netlify.com): *Add new site* → *Deploy manually* → arraste a pasta ou o .zip com o `index.html`.

## Como funciona
- Leitores não precisam de login. O contador de online conta quem estiver com o painel aberto.
- Editores clicam em *Entrar como editor* e digitam a senha. O navegador lembra a senha até clicar em *Sair do modo editor*.
- A senha fica protegida no banco: o painel só grava se a senha estiver certa. Para trocar, use *Alterar senha* no modo editor.
- A chave anon é pública por natureza. Quem protege os dados são as regras do `supabase.sql`.

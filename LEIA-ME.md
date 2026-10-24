# Publicar o DigiComi no Portal Digit

## 1. Supabase (uma vez)
SQL Editor → cola e corre `supabase.sql`. Cria `digicomi_itens`, acessível a qualquer colaborador com conta ativa no portal.

## 2. GitHub Pages
1. Cria o repositório **`Digit-ID/DigiComi`** (público).
2. Coloca `index.html` desta pasta na raiz.
3. Settings → Pages → "Deploy from a branch" → `main` → `/ (root)`.
4. Fica em **https://digit-id.github.io/DigiComi/**.

## 3. Portal Digit
Substitui o `index.html` do repositório `Digit-ID/Digit` pelo de `publicar/Digit/index.html` — já tem o cartão DigiComi.
(Alteração feita: nova entrada em `APPS` e texto do login.)

## Utilizadores
- Os mesmos do Portal Digit: quem tem conta ativa entra; admins do portal (`papel = admin`) são admins do DigiComi.
- A equipa de cada pessoa é o **departamento** do perfil no portal.
- Nada a gerir no DigiComi — a página Administração só mostra a lista (gestão no portal).
- Os nomes dos técnicos nas comissões devem coincidir com o nome no perfil do portal.
- No primeiro acesso de um admin, dados de teste guardados nesse browser sobem para a nuvem.

## Notas
- Sem sessão, a app redireciona para o portal. Dentro do portal, a sessão é passada automaticamente.
- A separação por departamento é feita na app; a base de dados garante que só colaboradores ativos leem/escrevem.
- Depois de publicar, força `Ctrl+Shift+R`.

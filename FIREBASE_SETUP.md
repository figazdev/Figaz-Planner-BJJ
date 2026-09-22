# Configuração Firebase — FÍGAZ PLANNER BJJ

## Serviços necessários

1. Authentication: habilitar E-mail/senha.
2. Firestore Database: criar em modo de produção.
3. Criar o primeiro usuário em Authentication > Users.
4. Copiar o UID do usuário.
5. No Firestore, criar a coleção `users` e um documento cujo ID seja o UID.
6. Campos do documento:
   - `role` (string): `admin`
   - `active` (boolean): `true`
   - `email` (string): e-mail do administrador
7. Publicar o arquivo `firestore.rules`.

A aplicação usa o documento:
`academies/figaz-planner-bjj/app/state`

Na primeira autenticação autorizada, os dados locais do dispositivo são enviados ao Firestore. Depois disso, o Firestore passa a ser a fonte compartilhada entre dispositivos.

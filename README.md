# Recuperação de senha

**RF**

- O usuário deve poder recuperar sua senha informando o seu email;
- O usuário deve receber um email com instruções de recuperação de senha;
- O usuário deve poder resetar sua senha;

**RNF**

- Utilizar o Mailtrap pata testar envios em ambiente de dev;
- Utilizar Amazon SES oara encios em produção;
- O envio de emails deve acontecer em segundo plano (background job);

**RN**

- O link eniado por email para resetar a senha ,deve expirar em 2h;
- O usuário precisa confirmar a nova senha ao resetar sua senha anterior;

# Atualização do perfil

**RF**

- O usuário deve poder atualuzar seu nome, email e senha.

**RN**

- O usuário não pode alterar seu email para um email já utilizado.
- Para ataulizar sua senha, o usuário deve informar a senha antiga.
- Par atualizar sua senha, o usuário deve confirmar a nova senha.

# Painel do prestador

**RF**

- O usuário deve poder lustar seus agendamentos de um dia específico;
- O prestador deve receber uma notificação sempre que houver um novo agendamento;
- O prestador deve poder visualizar as notificações não lidas;

**RNF**

- Os agendamentos do prestador no dia devem ser armazenados em cache;
- As notificações do prestador devem ser armazenadas no MongoDB;
- As notificações do prestador devem ser enciadas em tempo real utilizando Socket.io;

**RN**

- A notificação deve ter um status de lida ou não lida para que o prestador possa controlar;

# Agendamento de serviços

**RF**

- O usuário deve poder listar todos os prestadores de serviço cadastrados;
- O usuário deve poder listar os dias de um mês com pelo menos um horário disponível de um prestador;
- O usuário deve poder listar horários disponíveis em um dia específico de um prestador;
- O usuário deve poder realizar um novo agendamento com um prestador.

**RNF**

-A listagem de prestadores deve ser armazenada em cache;

**RN**

- Cada agendamento dve durar 1h exatamente;
- Os agendamentos devem estar disponíveis entre 8h às 18h (primeiro às 8, último às 17);
- O usuário não pode agendat em um horário já ocupado;
- O usuário não pode agendar em um horário que já passou;
- O usuário não pode agendar um horário consigo mesmo;

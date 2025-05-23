# ParrotTech OdontoPrev 🦷
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.4.3-green.svg)
![Java](https://img.shields.io/badge/Java-21-orange.svg)
![Azure OpenAI](https://img.shields.io/badge/Azure%20OpenAI-GPT--4o-blue.svg)

Sistema de gestão odontológica inteligente com integração de IA para assistência virtual e recomendações personalizadas de tratamento.

## 📋 Sobre o Projeto

O ParrotTech OdontoPrev é uma solução completa para modernizar o atendimento odontológico, desenvolvida como projeto da 4ª Sprint do curso FIAP. O sistema oferece gestão de pacientes, assistente virtual especializado em odontologia e sistema de recomendações baseado em inteligência artificial.

### 🎯 Objetivos do Projeto
- Digitalizar e otimizar o atendimento odontológico
- Implementar assistente virtual especializado em saúde bucal
- Gerar recomendações personalizadas de tratamento
- Oferecer interface moderna e intuitiva para profissionais da saúde

## 🚀 Tecnologias Utilizadas

### Backend
- **Java 21** - Linguagem principal
- **Spring Boot 3.4.3** - Framework principal
- **Spring MVC** - Framework para desenvolvimento de APIs REST e aplicações web seguindo o padrão Model-View-Controller
- **Spring Security** - Autenticação e autorização
- **Spring AI** - Integração com Azure OpenAI
- **Spring Data JPA** - Persistência de dados
- **Spring Boot Actuator** - Monitoramento e métricas
- **Maven** - Gerenciamento de dependências

### Frontend
- **Thymeleaf** - Engine de templates
- **Bootstrap 5** - Framework CSS responsivo
- **Font Awesome** - Ícones
- **JavaScript** - Interatividade

### Banco de Dados
- **Oracle Database** - Banco principal
- **Hibernate** - ORM

### Serviços Externos
- **Azure OpenAI Service** - GPT-4o para IA
- **Azure AI Studio** - Gerenciamento de modelos

## ✨ Funcionalidades Principais

### 🔐 Sistema de Autenticação Completo
- [x] Login seguro com Spring Security
- [x] Gestão de perfis (USER/ADMIN)
- [x] Proteção de rotas baseada em roles
- [x] Interface de login moderna e responsiva
- [x] Criptografia BCrypt para senhas

### 🤖 Assistente Virtual Inteligente
- [x] Chat em tempo real com IA especializada
- [x] Respostas contextualizadas sobre saúde bucal
- [x] Histórico de conversas mantido durante a sessão
- [x] Interface de chat moderna com indicadores de digitação
- [x] Sugestões de perguntas pré-definidas
- [x] Tratamento de erros e fallbacks

### 📊 Monitoramento e Métricas Avançadas
- [x] Health checks em tempo real
- [x] Métricas de performance da aplicação
- [x] Monitoramento de uso das APIs de IA
- [x] Cache inteligente para otimização
- [x] Contadores de sucesso/erro
- [x] Dashboard de estatísticas via Actuator

### 🎨 Interface Moderna e Responsiva
- [x] Design responsivo para todos os dispositivos
- [x] UX otimizada para profissionais da saúde
- [x] Tema customizado com cores da marca
- [x] Animações e feedback visual aprimorado
- [x] Acessibilidade e usabilidade

## 👥 Equipe de Desenvolvimento

| Membro | Função | GitHub |
|--------|--------|--------|
| **Julia Mariano** | Full Stack Developer | [@jumarianobf](https://github.com/jumarianobf) |
| **Leonardo Gaspar** | Full Stack Developer | [@Leonardo-Gaspar](https://github.com/Leonardo-Gaspar) |
| **Caio Eduardo** | Full Stack Developer | [@caioedum](https://github.com/caioedum) |


## 🛠️ Configuração e Instalação

### Pré-requisitos
✅ Java 21 ou superior
✅ Maven 3.6+
✅ Oracle Database (local ou remoto)
✅ Conta Azure OpenAI Service
✅ Git para clone do repositório


### Configuração do Azure OpenAI
1. Crie um recurso Azure OpenAI no portal Azure
2. Implante o modelo GPT-4o na região East US
3. Obtenha sua chave API e endpoint
4. Configure as variáveis de ambiente

### Variáveis de Ambiente Necessárias
Azure OpenAI
AZURE_OPENAI_API_KEY=sua-chave-aqui
AZURE_OPENAI_ENDPOINT=https://seu-recurso.openai.azure.com/

Banco de dados Oracle
DB_URL=jdbc:oracle:thin:@localhost:1521:ORCL
DB_USERNAME=seu-usuario
DB_PASSWORD=sua-senha


### Passos para Execução
1. Clone o repositório
git clone https://github.com/seu-usuario/parrottech-odontoprev.git

2. Entre no diretório
cd parrottech-odontoprev

3. Configure as variáveis de ambiente
No Windows:
set AZURE_OPENAI_API_KEY=sua-chave
set AZURE_OPENAI_ENDPOINT=seu-endpoint

No Linux/Mac:
export AZURE_OPENAI_API_KEY=sua-chave
export AZURE_OPENAI_ENDPOINT=seu-endpoint

4. Execute a aplicação
mvn spring-boot:run

5. Acesse no navegador
http://localhost:8080

## 🔗 Endpoints Principais

### 🌐 Endpoints Web (MVC)
| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/` | Página inicial |
| `GET` | `/login` | Tela de login |
| `GET` | `/assistente-odontologico` | Interface do chat |
| `POST` | `/assistente-odontologico` | Processar mensagens |

### 🚀 API REST
| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `POST` | `/api/assistente/consulta` | Consulta ao assistente via API |
| `GET` | `/api/recomendacoes/{usuarioId}` | Obter recomendações |

### 📊 Monitoramento (Actuator)
| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/actuator/health` | Status da aplicação |
| `GET` | `/actuator/metrics` | Métricas detalhadas |
| `GET` | `/actuator/info` | Informações da aplicação |

## ⚙️ Configurações Principais

### application.properties
Aplicação
spring.application.name=Challenge Odontoprev
server.port=8080

Banco de dados Oracle
spring.datasource.url=jdbc:oracle:thin:@187.8.12.142:1521:ORCL
spring.datasource.username=rm552713
spring.datasource.password=300305
spring.datasource.driver-class-name=oracle.jdbc.OracleDriver
spring.jpa.database-platform=org.hibernate.dialect.Oracle12cDialect
spring.jpa.hibernate.ddl-auto=update

Azure OpenAI
spring.ai.azure.openai.api-key=${AZURE_OPENAI_API_KEY}
spring.ai.azure.openai.endpoint=${AZURE_OPENAI_ENDPOINT}
spring.ai.azure.openai.deployment-name=gpt4o
spring.ai.azure.openai.chat.options.temperature=0.7
spring.ai.azure.openai.chat.options.max-tokens=800

Actuator
management.endpoints.web.exposure.include=*
management.endpoint.health.show-details=always

Cache
spring.cache.type=simple


## 🧪 Testando a Aplicação

### 👤 Usuários de Teste
| Usuário | Senha | Perfil |
|---------|-------|--------|
| `admin` | `admin` | ADMIN |
| `java` | `challenge` | USER |

### 💬 Casos de Teste do Chat IA
1. **Higiene Básica**: "Como escovar os dentes corretamente?"
2. **Problemas Comuns**: "O que causa sensibilidade dentária?"
3. **Prevenção**: "Quando devo trocar minha escova de dentes?"
4. **Doenças**: "O que é gengivite e como tratá-la?"
5. **Consultas**: "Com que frequência devo visitar o dentista?"

## 🔒 Segurança Implementada

- ✅ **Autenticação**: Spring Security com login personalizado
- ✅ **Autorização**: Controle de acesso baseado em roles
- ✅ **Criptografia**: Senhas protegidas com BCrypt
- ✅ **CSRF Protection**: Habilitada por padrão
- ✅ **Headers Seguros**: Configurados automaticamente
- ✅ **Variáveis de Ambiente**: Chaves API protegidas
- ✅ **Validação**: Entrada validada em todos endpoints

## 🐛 Solução de Problemas

### Problemas Comuns

**❌ Erro 400: "Unavailable model: gpt-4o"**
Solução: Verifique se o modelo está implantado no Azure OpenAI Studio



**❌ Respostas não aparecem no chat**
Solução: Verifique os logs para erros de extração de conteúdo



**❌ Erro de conexão com banco Oracle**
Solução: Verifique URL, usuário e senha no application.properties



### Logs Importantes
Verificar logs da aplicação
tail -f logs/application.log

Verificar status do Azure OpenAI
curl -H "api-key: $AZURE_OPENAI_API_KEY"
"$AZURE_OPENAI_ENDPOINT/openai/deployments"


## 🤝 Contribuindo

1. Faça fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add: Nova funcionalidade incrível'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

### Padrões de Commit
- `Add:` Nova funcionalidade
- `Fix:` Correção de bug
- `Update:` Atualização de funcionalidade
- `Remove:` Remoção de código

## 📝 Roadmap Futuro

### Versão 2.0 🚀
- [ ] **Análise de Imagens**: Upload e análise de radiografias
- [ ] **Agendamento IA**: Sistema inteligente de agendamentos
- [ ] **Dashboard Analytics**: Relatórios e estatísticas avançadas
- [ ] **Aplicativo Mobile**: App nativo iOS/Android

### Versão 2.5 🌟
- [ ] **IoT Integration**: Conectividade com equipamentos dentários
- [ ] **Telemedicina**: Consultas virtuais integradas
- [ ] **Blockchain**: Histórico médico imutável
- [ ] **API Pública**: Integração com sistemas terceiros


## 🏆 Conquistas Sprint 4

- ✅ **100% das funcionalidades** solicitadas implementadas
- ✅ **Integração completa** com Azure OpenAI
- ✅ **Interface moderna** e responsiva
- ✅ **Segurança robusta** com Spring Security
- ✅ **Monitoramento avançado** com Actuator
- ✅ **Arquitetura escalável** e bem documentada

---

*Desenvolvido pela equipe ParrotTech para a 4ª Sprint FIAP 2025*

**"Inovando o futuro da odontologia com inteligência artificial"**

---

**Última atualização**: Maio 2025  
**Versão**: 1.0.0  

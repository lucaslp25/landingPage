# Lavita Code – Landing Page Profissional

![Angular CI](https://github.com/LavitaCode/landpage-lavita/actions/workflows/angular.yml/badge.svg)

Landing page institucional da Lavita Code – softhouse especialista em **apps**, **sistemas web**, **e-commerces** e **jog**

> Dúvidas? Fale com o responsável: rafasdiasdev@gmail.com
> 

---

## 📚 Sumário

- [Visão Geral](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Navegação Rápida](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Pré-requisitos](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Instalando o Angular CLI](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Criando o Projeto Angular](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Git e Primeira Subida para o Repositório](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Padrão de Estrutura de Pastas](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [O que são Models?](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [O que são Serviços (Services)?](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Gerando Componentes e Serviços](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Exemplo de Bind de Dados - Services + Components](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Montando a Landing Page](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Rotas e Navegação Angular](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Controle de Versionamento Profissional (Commits e Branches)](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Workflow GitHub: Branch, Commit, PR](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Configuração do CI/CD (GitHub Actions)](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Checklist de Entrega](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [FAQ & Boas Práticas](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)

---

## Visão Geral

Este projeto tem como objetivo **apresentar a Lavita Code e treinar o desenvolvimento profissional de uma aplicação Angular** seguindo padrões modernos:

- Organização de pastas escalável
- Clean Code (código limpo e claro)
- Uso de tipagem total (TypeScript interfaces/models para todos os dados)
- GitHub Flow (branch para cada feature, PR, revisão, merge)
- Integração contínua (CI/CD)
- Comunicação entre componentes via serviços
- Documentação e onboarding automatizados

---

## Navegação Rápida

- [Como rodar localmente](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Como contribuir](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Exemplo de commit](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)
- [Dúvidas frequentes](https://www.notion.so/23462e22cbef80009e5ec1a7e15b4c1b?pvs=21)

---

## Pré-requisitos

- **Node.js** >= 20 ([baixar](https://nodejs.org/))
- **npm** (vem com o Node.js)
- **Git** ([baixar](https://git-scm.com/))
- **Conta no GitHub**

---

## Instalando o Angular CLI

O Angular CLI (Command Line Interface) é a principal ferramenta para gerar, servir, compilar e criar componentes/serviços no Angular.

```
npm install -g @angular/cli

```

Verifique a versão:

```
ng version

```

---

## Criando o Projeto Angular

1. No terminal, clone o repositório vazio:
    
    ```
    git clone git@github.com:LavitaCode/landpage-lavita.git
    cd landpage-lavita
    
    ```
    
2. Crie o projeto Angular:
    
    ```
    ng new landpage-lavita
    cd landpage-lavita
    
    ```
    
    - **Standalone Components:** escolha sim (Angular 17+ já faz por padrão)
    - **Routing:** sim
    - **Estilo:** SCSS
3. Remova qualquer [README.md](http://readme.md/) criado automaticamente e substitua por este.

---

## Git e Primeira Subida

1. **Inicialize o git** (caso não tenha sido feito):
    
    ```
    git init
    
    ```
    
2. **Ajuste o remote** (se necessário):
    
    ```
    git remote add origin git@github.com:LavitaCode/landpage-lavita.git
    
    ```
    
3. **Commit inicial:**
    
    ```
    git add .
    git commit -m "chore(init): estrutura base do projeto Angular"
    git branch -M main
    git push -u origin main
    
    ```
    

---

## Padrão de Estrutura de Pastas

```
src/app/
│
├── components/
│   ├── hero/
│   ├── about/
│   ├── solution-showcase/
│   ├── testimonials/
│   ├── cta-final/
│
├── shared/
│   ├── navbar/
│   ├── footer/
│   ├── solution-card/
│   ├── testimonial-card/
│
├── core/
│   ├── services/
│   │   ├── testimonial.service.ts
│   │   ├── event-bus.service.ts
│   ├── models/
│   │   ├── testimonial.model.ts
│   │   ├── solution.model.ts
│   │   ├── call-to-action.model.ts
│   │   ├── menu-link.model.ts
│   │   ├── contact-request.model.ts
│
├── app.component.ts
├── app.component.html
├── app.routes.ts

```

---

## O que são Models?

**Model** (ou interface, ou tipagem) é a **definição formal de como um dado deve ser representado em TypeScript**.

**Por que usar models?**

- Padroniza estrutura de dados
- Reduz bugs de tipagem
- Facilita auto-complete e validação do editor
- Documenta o que cada entidade (depoimento, serviço, menu, etc) deve conter

### Exemplo real:

**src/app/core/models/testimonial.model.ts**

```
export interface Testimonial {
  id: string;
  name: string;
  companyOrArea: string;
  content: string;
  avatarUrl: string;
  date: string;
}

```

Crie um arquivo para **cada tipo de dado**: depoimento, solução, CTA, menu, contato, etc.

---

## O que são Serviços (Services)?

**Services** são classes que encapsulam lógica de negócio, **reúso de dados**, comunicação entre componentes, acesso a APIs e mais.
No Angular, usamos o decorator `@Injectable` para declarar um service.

### Tipos de serviços comuns neste projeto:

- **Services de dados:** fornecem arrays tipados para uso em componentes (ex: depoimentos)
- **EventBusService:** permite um componente emitir eventos e outro reagir, sem acoplamento direto (padrão RxJS Subject/Observable)

### Exemplo prático – Service de depoimentos (mock):

**src/app/core/services/testimonial.service.ts**

```
import { Injectable } from '@angular/core';
import { Testimonial } from '../models/testimonial.model';

@Injectable({ providedIn: 'root' })
export class TestimonialService {
  getTestimonials(): Testimonial[] {
    return [
      {
        id: '1',
        name: 'Ana Souza',
        companyOrArea: 'E-commerce',
        content: 'A Lavita revolucionou nosso negócio digital!',
        avatarUrl: '/assets/ana.jpg',
        date: '2024-07-18'
      },
      // ...outros depoimentos
    ];
  }
}

```

---

## Gerando Componentes e Serviços

Gere cada componente individualmente com o Angular CLI:

```
ng generate component shared/navbar
ng generate component shared/footer
ng generate component shared/solution-card
ng generate component shared/testimonial-card

ng generate component components/hero
ng generate component components/about
ng generate component components/solution-showcase
ng generate component components/testimonials
ng generate component components/cta-final

```

Gere os serviços principais:

```
ng generate service core/services/testimonial
ng generate service core/services/event-bus

```

---

## Exemplo de Bind de Dados - Services + Components

**Bind** é o termo usado para conectar os dados do service ao template do componente na tela.

### Exemplo prático: Consumir depoimentos mockados no componente Testimonials

**src/app/components/testimonials/testimonials.component.ts**

```
import { Component } from '@angular/core';
import { TestimonialService } from '../../core/services/testimonial.service';
import { Testimonial } from '../../core/models/testimonial.model';

@Component({
  selector: 'app-testimonials',
  templateUrl: './testimonials.component.html',
  styleUrls: ['./testimonials.component.scss'],
  standalone: true,
  imports: []
})
export class TestimonialsComponent {
  testimonials: Testimonial[] = [];

  constructor(private testimonialService: TestimonialService) {}

  ngOnInit() {
    this.testimonials = this.testimonialService.getTestimonials();
  }
}

```

**src/app/components/testimonials/testimonials.component.html**

```html
<section>
  <h2>O que nossos clientes dizem</h2>
  <div *ngFor="let depo of testimonials">
    <img [src]="depo.avatarUrl" alt="Foto de {{depo.name}}" width="50" />
    <strong>{{depo.name}}</strong> ({{depo.companyOrArea}})
    <p>{{depo.content}}</p>
    <small>{{depo.date}}</small>
    <hr />
  </div>
</section>

```

**Pontos importantes:**

- Sempre tipar arrays e variáveis (`Testimonial[]`)
- Fazer o bind de dados (Angular usa o `ngFor` para repetir cada depoimento)
- Qualquer alteração no service automaticamente reflete na tela após reload

---

## Montando a Landing Page

No arquivo `app.component.html`, monte os blocos nesta ordem:

```html
<app-navbar />
<app-hero />
<app-about />
<app-solution-showcase />
<app-testimonials />-
<app-cta-final />
<app-footer />

```

Todos os componentes devem ser importados no array `imports` do `@Component` de `app.component.ts`.

---

## Rotas e Navegação Angular

- Utilize o arquivo `app.routes.ts` para criar rotas como `/sobre`, `/servicos`, `/contato`.
- Exemplo:
    
    ```
    import { Routes } from '@angular/router';
    import { AboutComponent } from './components/about/about.component';
    
    export const routes: Routes = [
      { path: '', component: HeroComponent },
      { path: 'sobre', component: AboutComponent },
      // outras rotas...
    ];
    
    ```
    

---

## Controle de Versionamento Profissional (Commits e Branches)

### Por que usar convenção de commits?

- **Clareza:** Facilita entender o histórico do projeto.
- **Automação:** Permite gerar changelogs automáticos, releases, e integrações CI/CD.
- **Padronização:** Todos do time falam a mesma "língua", sem ruído.
- **Auditoria:** Fica fácil ver onde foi feita cada alteração, bug ou feature.
- **Revisão:** O PR mostra claramente o que está entrando e por quê.

### Convenção utilizada: [Conventional Commits](https://www.conventionalcommits.org/)

A mensagem segue a estrutura:

```
tipo(nome-do-bloco): mensagem breve e objetiva

```

**Exemplos:**

- `feat(hero): adiciona componente hero com headline animada`
- `fix(footer): corrige erro de padding no mobile`
- `docs(readme): atualiza documentação de onboarding`
- `style(navbar): ajusta cores e espaçamento`
- `refactor(testimonials): extrai lógica de filtro para service`
- `test(solution-showcase): adiciona testes unitários para exibição de cards`
- `chore(ci): ajusta configuração do pipeline`

### **Tipos mais usados:**

- `feat`: nova funcionalidade (feature)
- `fix`: correção de bug
- `docs`: documentação apenas
- `style`: mudança de formatação, sem alterar lógica (ex: identação, espaço, CSS puro)
- `refactor`: refatoração de código, sem mudança de comportamento externo
- `test`: criação ou ajuste de testes
- `chore`: tarefas auxiliares (scripts, configs, dependências, ci)

**Quando usar cada tipo?**

| Tipo | Quando usar |
| --- | --- |
| feat | Toda vez que criar ou alterar uma funcionalidade visível ao usuário |
| fix | Qualquer correção de bug/erro, seja visual, funcional ou de lógica |
| docs | Alterações ou inclusão apenas de documentação (README, comentários) |
| style | Mudanças puras de visual, CSS, padronização, sem impacto em lógica |
| refactor | Quando melhorar a estrutura do código sem alterar comportamento do sistema |
| test | Sempre que adicionar, corrigir ou remover testes automatizados |
| chore | Mudanças de infraestrutura, configs, scripts, pipeline, dependências (sem impacto funcional) |

---

### **Padrão de nomes de branches**

Utilize o padrão:

```
<tipo>/<nome-curto-descritivo>

```

**Exemplos reais:**

- `feature/navbar`
- `feature/solution-showcase-carousel`
- `fix/navbar-mobile`
- `fix/testimonials-avatar-bug`
- `docs/readme-getting-started`
- `refactor/eventbus-communication`
- `chore/update-angular-19`

### **Dicas para nome de branch:**

- Use sempre minúsculas, separado por  (kebab-case).
- O prefixo principal mais comum é `feature/` (nova funcionalidade).
- Use `fix/` para correção de bugs.
- Use `refactor/`, `docs/`, `test/`, `chore/` conforme o tipo da mudança.
- Seja **específico** e evite nomes genéricos como `feature/ajustes` ou `fix/bugzinho`.
- Evite acentos, espaços ou caracteres especiais.

---

### **Fluxo padrão para cada nova feature ou ajuste:**

1. Crie uma branch específica:
    
    ```
    git checkout -b feature/hero-animation
    
    ```
    
2. Faça seus commits seguindo o padrão de mensagens (commit pequeno, claro e atômico):
    
    ```
    git add .
    git commit -m "feat(hero): adiciona animação de entrada no headline"
    
    ```
    
3. Ao finalizar, suba sua branch e crie um Pull Request para `main`:
    
    ```
    git push origin feature/hero-animation
    
    ```
    
4. No PR, descreva brevemente o que foi feito. Aguarde revisão e só faça merge após aprovação e CI verde.

---

### **Resumo Visual**

| Tipo de branch | Para quê usar | Exemplo |
| --- | --- | --- |
| feature/ | Novas funcionalidades | feature/hero, feature/cta |
| fix/ | Correções de bug | fix/footer-mobile, fix/404 |
| docs/ | Apenas documentação | docs/readme-estrutura |
| refactor/ | Refatoração de código | refactor/navbar-service |
| chore/ | Infra, configs, dependências | chore/update-angular |
| test/ | Testes unitários, e2e, mocks | test/navbar-service |

---

> Nunca use main ou master diretamente. Nunca suba várias funcionalidades/ajustes misturados na mesma branch ou PR.
Cada branch/PR = 1 objetivo, 1 revisão, 1 merge seguro!
> 

---

**Ficou com dúvida? Escreva sua mensagem de commit e branch no PR — a equipe está aqui para ajudar.**

---

## Workflow GitHub: Branch, Commit, PR

### Sempre crie uma branch para cada feature

```
git checkout -b feature/<nome-da-feature>
# Exemplo: feature/navbar

```

### Commits claros, pequenos e padronizados (conventional commits)

```
git add .
git commit -m "feat(navbar): cria componente de navegação principal"

```

### Suba sua branch e crie um PR

```
git push origin feature/navbar

```

No GitHub, crie um Pull Request para a `main`, aguarde revisão, só faça merge após CI verde.

> Nunca desenvolva direto na main. Nunca misture mais de uma feature na mesma PR.
> 

---

## Configuração do CI/CD (GitHub Actions)

Crie o arquivo `.github/workflows/angular.yml`:

```yaml
name: Angular CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Use Node.js 20
        uses: actions/setup-node@v3
        with:
          node-version: 20
      - run: npm ci
      - run: npm run build --if-present
      - run: npm test --if-present

```

> O pipeline roda a cada push ou PR na main. Só faça merge se CI/CD estiver verde!
> 

---

## Checklist de Entrega

- [ ]  Estrutura criada conforme padrão sênior deste guia
- [ ]  Models para **todos** os dados (depoimentos, soluções, menu, cta, contato etc.)
- [ ]  Cada componente em branch separada, PR para cada feature
- [ ]  Commits SEMPRE padronizados (`feat`, `fix`, `docs`, `style`, etc)
- [ ]  CI funcionando em PR e main
- [ ]  [README.md](http://readme.md/) atualizado, didático, com navegação
- [ ]  Comunicação entre componentes via EventBus Service
- [ ]  Dados mockados sempre tipados

---

## FAQ & Boas Práticas

- **O que é Standalone Component?**
Componente Angular independente, sem necessidade de módulo. Padrão desde Angular 17+.
- **O que é CTA?**
“Call To Action” — bloco que chama o visitante para agir, ex: “Solicitar Orçamento”.
- **Como funciona a comunicação entre componentes?**
Use services como EventBus, nunca variáveis globais ou métodos

diretos.

- **Por que preciso tipar tudo, até menu/footer?**
Tipagem força clareza, segurança e auto-documentação do projeto. Use sempre interfaces.
- **Não misture features em uma PR!**
Cada feature deve ser revisada, testada e integrada separadamente.
- **Como testar tipagem?**
Tente passar uma propriedade errada em um array de model – o TypeScript avisa na hora!
Use sempre auto-complete e corrija o que o editor apontar.

---

**Dúvidas?**
Fale com o responsável: [rafasdiasdev@gmail.com](mailto:rafasdiasdev@gmail.com)

Bons commits, boas PRs e excelente código.
Time Lavita Code & Ayla
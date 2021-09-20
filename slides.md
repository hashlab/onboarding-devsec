---
theme: default
class: 'text-center'
background: https://tech-culture.hash.com.br/_next/image?url=https%3A%2F%2Fsuper-static-assets.s3.amazonaws.com%2F4eb5bada-97e6-4a1f-9899-2f3cd62679af%2Fimages%2Ff0c54c1d-5fdc-4168-a997-b7708f99e69f.jpg&w=3840&q=100
highlighter: shiki
info: |
  ## OWASP Top 10
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
---

# OWASP Top 10 2017

As 10 vulnerabilidades mais críticas da internet.

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 p-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Vamos la! <carbon:arrow-right class="inline"/>
  </span>
</div>

<a href="https://github.com/hashlab" target="_blank" alt="GitHub"
  class="abs-br m-6 text-xl icon-btn opacity-50 !border-none !hover:text-white">
  <carbon-logo-github />
</a>

---

<span class="text-2xl font-bold">Time Security</span>

<div class="flex justify-between">
    <div class="grid grid-cols-4 gap-5">
    <v-click>
      <div class="rounded-lg bg-gray-700 p-3">
        <img
          src="/luisa.jpg"
          class="w-35"
          border="rounded-lg"
          title="Luisa Soares"
          alt="Luisa Soares"
        />
        <span class="block">Luisa Soares</span>
        <span class="text-xs my-1 block">Head of Legal and Security</span>
      </div>
    </v-click>
    <v-click>
      <div class="rounded-lg bg-gray-700 p-3">
        <img
          src="/juliano.jpg"
          class="w-35"
          border="rounded-lg"
          title="Juliano Dapper"
          alt="Juliano Dapper"
        />
        <span class="block">Juliano Dapper</span>
        <span class="text-xs my-1 block">Manager</span>
      </div>
    </v-click>
    <v-click>
      <div class="rounded-lg bg-gray-700 p-3">
        <img
          src="/bruno.jpg"
          class="w-35"
          border="rounded-lg"
          title="Bruno Garcia"
          alt="Bruno Garcia"
        />
        <span class="block">Bruno Garcia</span>
        <span class="text-xs my-1 block">Information Security Analyst</span>
      </div>
    </v-click>
    <v-click>
      <div class="rounded-lg bg-gray-700 p-3">
        <img
          src="/yara.jpg"
          class="w-35"
          border="rounded-lg"
          title="Yara Rodrigues"
          alt="Yara Rodrigues"
        />
        <span class="block">Yara Rodrigues</span>
        <span class="text-xs my-1 block">Information Security Analyst</span>
      </div>
    </v-click>
    <v-click>
      <div class="rounded-lg bg-gray-700 p-3">
        <img
          src="/pedro.jpg"
          class="w-35"
          border="rounded-lg"
          title="Pedro Bittencourt"
          alt="Pedro Bittencourt"
        />
        <span class="block">Pedro Bittencourt</span>
        <span class="text-xs my-1 block">PCI Specialist</span>
      </div>
    </v-click>
    <v-click>
      <div class="rounded-lg bg-gray-700 p-3">
        <img
          src="/guisso.jpg"
          class="w-35"
          border="rounded-lg"
          title="Fernando Guisso"
          alt="Fernando Guisso"
        />
        <span class="block">Fernando Guisso</span>
        <span class="text-xs my-1 block">Security Software Engineer</span>
      </div>
    </v-click>
    <v-click>
      <div class="rounded-lg bg-gray-700 p-3">
        <img
          src="/marcos.jpg"
          class="w-35"
          border="rounded-lg"
          title="Marcos Nunes"
          alt="Marcos Nunes"
        />
        <span class="block">Marcos Nunes</span>
        <span class="text-xs my-1 block">LGPD Specialist</span>
      </div>
    </v-click>
    </div>
  </div>

---
layout: image-right
image: https://s3.amazonaws.com/super-notion/images/34a18b0d-bd76-44bb-ab9a-4fe3c9ce9221.png
---

# OWASP

O OWASP (Open Web Application Security Project), ou Projeto Aberto de Segurança em Aplicações Web, é uma comunidade online que cria e disponibiliza de forma gratuita artigos, metodologias, documentação, ferramentas e tecnologias no campo da segurança de aplicações web.

[OWASP.org](https://owasp.org)

---
layout: image-left
image: https://super-static-assets.s3.amazonaws.com/4eb5bada-97e6-4a1f-9899-2f3cd62679af/images/9d76b419-5f67-4c40-b976-cbbf29e7805e.png
---

# OWASP Top 10

- 📝 <v-click>**Injeção**</v-click>
- 🧑‍💻 <v-click>**Quebra de Autenticação**</v-click>
- 🎨 <v-click>**Exposição de dados sensiveis**</v-click>
- 🤹 <v-click>**XXE / Entidades Externas de XML**</v-click>
- 🎥 <v-click>**Quebra no controle de acesso**</v-click>
- 📤 <v-click>**Configuração de segurança incorretas**</v-click>
- 🛠 <v-click>**XSS**</v-click>
- 🤹 <v-click>**Desserializacão insegura**</v-click>
- 🎨 <v-click>**Uso de componentes com vulnerabilidades conhecidas**</v-click>
- 🛠 <v-click>**Registro e monitoração insuficiente**</v-click>

[OWASP Top 10](https://owasp.org/www-project-top-ten)

---

# Injeção

<div grid="~ cols-2 gap-4">
<div>
Falhas de injeção, tais como injeções de SQL, OS e LDAP ocorrem quando dados não-confiáveis são enviados para um interpretador como parte de um comando ou consulta legítima.

Os dados hostis do atacante podem enganar o interpretador levando-o a executar comandos não pretendidos ou a aceder a dados sem a devida autorização.

<v-click>

### Java SQLi
```java {1,2|3|all}
String query = "SELECT * FROM accounts WHERE userID='"
                + request.getParameter("id") + "'";
id=' or 1=1--
```
</v-click>

</div>

<div>

<v-click>

### Node NoSQLi
```js {1-4|6|10-14|17|all}
let query = {
	username: req.body.username,
	password: req.body.password
}

User.find(query, function (err, user) {
	if (err) {
        // handle error
	} else {
		res.json({
            role: user[0].role,
            username: user[0].username,
            msg: "Correct!"
        });
	}
});
{"username":"myaccount","password":{"$ne": 1}}
```
</v-click>

</div>
</div>

---

# Quebra de Autenticação

<div grid="~ cols-2 gap-4">
<div>
As funções da aplicação que estão relacionadas com a autenticação e gestão de sessões são muitas vezes implementadas incorretamente, permitindo que um atacante possa comprometer passwords, chaves, tokens de sessão, ou abusar doutras falhas da implementação que lhe permitam assumir a identidade de outros utilizadores (temporária ou permanentemente).
</div>

<div>

<v-click>

### Python Wordlist bruteforce
```python {3|4|5|6|8|9-11|12-14|all}
import requests

url = "http://localhost:3000/rest/user/login"
params = {"email":"admin@juice-sh.op","password":""}
wordlist = open("wordlist.txt", "r")
linhas = wordlist.readlines()

for index, line in enumerate(linhas):
    params["password"] = line.rstrip("\n")
    tentativa_login = requests.post(url,params)
    print("Tentativa {}, Senha: {}".format(index, senha))
    if tentativa_login.status_code != 401:
        print("Achei a senha: {}".format(senha))
        break
```
</v-click>

</div>

</div>

---

# Exposição de dados sensiveis

<div grid="~ cols-2 gap-4">
<div>
Muitas aplicações web e APIs não protegem de forma adequada dados sensíveis, tais como dados financeiros, de saúde ou dados de identificação pessoal (PII). Os atacantes podem roubar ou modificar estes dados mal protegidos para realizar fraudes com cartões de crédito, roubo de identidade, ou outros crimes. Os dados sensíveis necessitam de proteções de segurança extra como encriptação quando armazenados ou em trânsito, tal como precauções especiais quando trocadas com o navegador web.
</div>

</div>

---

# XXE

<div grid="~ cols-2 gap-4">
<div>
Muitos processadores de XML mais antigos ou mal configurados avaliam referências a entidades externas dentro dos documentos XML. Estas entidades externas podem ser usadas para revelar ficheiros internos usando o processador de URI de ficheiros, partilhas internas de ficheiros, pesquisa de portas de comunicação internas, execução de código remoto e ataques de negação de serviço, tal como o ataque Billion Laughs.

<v-click>

### Billions Laught attack
```xml {4-7|10|all}
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE foo [
  <!ELEMENT foo ANY>
  <!ENTITY bar "World ">
  <!ENTITY t1 "&bar;&bar;">
  <!ENTITY t2 "&t1;&t1;&t1;&t1;">
  <!ENTITY t3 "&t2;&t2;&t2;&t2;&t2;">
]>
<foo>
  Hello &t3;
</foo>
```
</v-click>

</div>

<div>

<v-click>

### SSRF
```xml {4,5,10|6,7,11|all}
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE foo [
  <!ELEMENT foo ANY>
  <!ENTITY xxe SYSTEM
  "file:///etc/passwd">
  <!ENTITY internaladdrs SYSTEM
  "http://192.168.0.1/secret.txt">
]>
<foo>
  &xxe;
  &internaladdrs;
</foo>
```
</v-click>
</div>

</div>

---

# Quebra no controle de acesso

<div grid="~ cols-2 gap-4">
<div>
As restrições sobre o que os utilizadores autenticados estão autorizados a fazer nem sempre são corretamente verificadas. Os atacantes podem abusar destas falhas para aceder a funcionalidades ou dados para os quais não têm autorização, tais como dados de outras contas de utilizador, visualizar ficheiros sensíveis, modificar os dados de outros utilizadores, alterar as permissões de acesso, entre outros.
</div>

<div>

<v-click>

### Unprotected admin page
```js {5-7|6|all}
var isAdmin = false;
if (isAdmin) {
  ...
  var adminPanelTag = document.createElement('a');
  adminPanelTag.setAttribute(
    'https://insecure-website.com/administrator-panel'
  );
  adminPanelTag.innerText = 'Admin panel';
  ...
}
```
</v-click>

</div>
</div>

---

# Configuração de segurança incorretas

<div grid="~ cols-2 gap-4">
<div>
As más configurações de segurança são o aspeto mais observado nos dados recolhidos. Normalmente isto é consequência de configurações padrão inseguras, incompletas ou ad hoc, armazenamento na nuvem sem qualquer restrição de acesso, cabeçalhos HTTP mal configurados ou mensagens de erro com informações sensíveis. Não só todos os sistemas operativos, frameworks, bibliotecas de código e aplicações devem ser configurados de forma segura, como também devem ser atualizados e alvo de correções de segurança atempadamente.
</div>
<div>

<v-click>

### seu roteador
```
192.168.0.1
user: Admin
pass: admin
```
</v-click>

<v-click>

### Apache/Nginx serving sensitive files
```txt
https://insecure-site.com/.git
https://insecure-site.com/.env
https://insecure-site.com/go.mod
https://insecure-site.com/package.json
https://insecure-site.com/requirements.txt
https://insecure-site.com/src/...

```
</v-click>

</div>

</div>

---

# XSS

<div grid="~ cols-2 gap-4">
<div>
As falhas de XSS ocorrem sempre que uma aplicação inclui dados não-confiáveis numa nova página web sem a validação ou filtragem apropriadas, ou quando atualiza uma página web existente com dados enviados por um utilizador através de uma API do browser que possa criar JavaScript. O XSS permite que atacantes possam executar scripts no browser da vítima, os quais podem raptar sessões do utilizador, descaraterizar sites web ou redirecionar o utilizador para sites maliciosos.
</div>
<div>

<v-click>

### prank
```html
 <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay"
 src="http://ellisonleao.github.io/clumsy-bird/">
 </iframe>
```
</v-click>

<v-click>

### get localStorage
```html
<image src=1 href=1
    onerror="javascript:alert(localStorage[0])">
</image>
```
</v-click>

</div>
</div>

---

# Desserializacão insegura

<div grid="~ cols-2 gap-4">
<div>
Desserialização insegura normalmente leva à execução remota de código. Mesmo que isto não aconteça, pode ser usada para realizar ataques, incluindo ataques por repetição, injeção e elevação de privilégios.
</div>
<div>

<v-click>

### java object deserialization
```java {1|3-6|all}
O:4:"User":2:{s:8:"username";s:6:"carlos";s:7:"isAdmin";b:0;}

$user = unserialize($_COOKIE);
if ($user->isAdmin === true) {
// allow access to admin interface
}
```
</v-click>

</div>
</div>

---

# Uso de componentes com vulnerabilidades conhecidas

<div grid="~ cols-2 gap-4">
<div>
Componentes tais como, bibliotecas, frameworks e outros módulos de software, são executados com os mesmos privilégios que a aplicação. O abuso dum componente vulnerável pode conduzir a uma perda séria de dados ou controlo completo de um servidor. Aplicações e APIs que usem componentes com vulnerabilidades conhecidas podem enfraquecer as defesas da aplicação possibilitando ataques e impactos diversos.
</div>

</div>

---

# Registro e monitoração insuficiente

<div grid="~ cols-2 gap-4">
<div>
O registo e monitorização insuficientes, em conjunto com uma resposta a incidentes inexistente ou insuficiente permite que os atacantes possam abusar do sistema de forma persistente, que o possam usar como entrada para atacar outros sistemas, e que possam alterar, extrair ou destruir dados. Alguns dos estudos demonstram que o tempo necessário para detetar uma violação de dados é de mais de 200 dias e é tipicamente detetada por entidades externas ao invés de processos internos ou monitorização.
</div>

</div>

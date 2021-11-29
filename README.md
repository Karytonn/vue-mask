
# Vue Input Mask

Máscara de inputs simples para VueJS e NuxtJs

## Principais tipos de entradas (inputs)

- CPF
- CNPJ
- Telefone
- ... e muito mais

## Documentação oficial

[Vue The Mask](https://vuejs-tips.github.io/vue-the-mask/)

## Utilizando em projetos NuxtJS

1) Primeiro instale a dependência

```bash
$ yarn add vue-the-mask
or
$ npm i -S vue-the-mask
````

2) Crie um plugin para instanciar o `VueTheMask`

Esse deve ser o caminho da pasta: *plugins/mask.js*

Esse deve ser o conteúdo do plugin:

```javascript
import Vue from 'vue'
import VueTheMask from 'vue-the-mask'
Vue.use(VueTheMask)
````

3) Declare o plugin no seu arquivo de configuração `nuxt.config.js`

```javascript
plugins: [
    "@/plugins/mask"
  ],
```

4) Aplique a máscara ao seu imput

*Existe 3 formas de se fazer isso, no meu caso prefiro via diretiva, conforme o exemplo abaixo*

```javascript
<label for="tel" class="label" >Com mascará</label>
<input id="tel" class="input" type="tel" placeholder="(62) 98888-7777" v-mask="['(##) ####-####', '(##) #####-####']">
```

**Nesse repositório contem a implementação em NuxtJS citada acima.**

## Utilizando em projetos VueJS CLI

1) Primeiro instale a dependência

```bash
$ yarn add vue-the-mask
or
$ npm i -S vue-the-mask
````

2) Importe o `VueTheMask` no componente 

*Existe 3 formas de se fazer isso, no meu caso prefiro via diretiva, conforme o exemplo abaixo*

```javascript
import {mask} from 'vue-the-mask'
export default {
  directives: {mask}
}
````

3) Aplique a máscara ao seu imput

```javascript
<label for="tel" class="label" >Com mascará</label>
<input id="tel" class="input" type="tel" placeholder="(62) 98888-7777" v-mask="['(##) ####-####', '(##) #####-####']">
```

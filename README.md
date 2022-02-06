# Nuxt-App Portfolio : Form Based Expert System for Eye Disease Screening System

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## Next.js (React.js Framework) and Nuxt.js (Vue.js Framework) Similarities

List of similiarities function or whatever it called that sometimes make me confused.

### 1. Looping inside component (React | Vue)

--- in React ---

`data.map((i,index) => (<some JSX>))`

--- in Vue ---

`<div v-for="(i,index) in data">some HTML</div>`

### 2. Key for index (React | Vue)

--- in React ---

`<div key={}>some HTML</div>`

--- in Vue ---

`<div :key="">some HTML</div>`

### 3. Link (React in JSX | Vue in Vue Template)

--- in React ---

`href=""`

--- in Vue ---

`:href=""`

### 4. Validator (React in JSX | Vue in Vue Template)

--- in React ---

`{isTrue? ({<div>some HTML</div>})}`

--- in Vue ---

`<div v-if="isTrue">{some HTML}</div>`

### 5. Input change handler (React | Vue)

--- in React ---

`<input value={email} onChange={(e) => {setEmail(e.target.value)}} type=""/> `

--- in Vue ---

`<input v-model="email" type=""/> `

or 

`<input v-on:change="email($event)" :value="email" />`

or 

`<input :value="email" @input="email = $event" />`

### 6. State (React | Vue)

--- in React ---

`const [data, setData] = useState("");`

--- in Vue ---

`data(){ return { data:"", } }`

or

`data: () => ({ data:"" })`

### 7. Set New Value in a State (React | Vue)

--- in React ---

`setData(newValude)`

--- in Vue ---

`this.data = newValue`

### 8. Passing Data (React in JSX | Vue in Vue Template)

--- in React ---

`{ data }`

--- in Vue ---

`{{ data }}`

## Reference 

1. Create a sticky navbar : https://developer.mozilla.org/en-US/docs/Web/CSS/position

2. Set background color full screen height : https://www.geeksforgeeks.org/how-to-set-a-background-color-to-full-page-using-tailwind-css/

3. Using axios in Nuxt.js : https://axios.nuxtjs.org/options

4. Set v-model in checkbox array : https://www.nicesnippets.com/blog/vue-js-get-checked-value-of-checkbox-if-use-array-as-a-model

5. Using this.$router.push() in Nuxt.js : https://stackoverflow.com/questions/50375244/push-a-route-moving-from-vuejs-to-nuxtjs

6. Using redirect() : https://nuxtjs.org/docs/internals-glossary/context#redirect

7. Save token on local storage using Vue.js : https://stackoverflow.com/questions/64665017/how-to-save-simple-jwt-token-in-local-storage-using-vue-js-vuex-and-django-rest

## Error

Error that I found when building this portfolio.

1. Problem : [Vue warn]: Avoid using non-primitive value as key, use string/number value instead

Solution : https://stackoverflow.com/questions/53420082/vue-warn-avoid-using-non-primitive-value-as-key-use-string-number-value-inst

2. Problem : Classname='' is not working in Nuxt.js

Solution : Using Class='' instead.

3. Problem : bg-color tailwind is not working in Nuxt.js <main> tag

Solution : https://stackoverflow.com/questions/65812581/tailwind-custom-colors-default-not-working

4. Problem : Using checkbox

Solution : https://stackoverflow.com/questions/41001192/setting-a-checkbox-as-checked-with-vue-js

5. Problem : Created(){} in Nuxt.js error, but in Vue.js is not.

Solution : Just delete Created(){} in export default {} inside <script></script>

6. Problem : Cannot read properties of undefined (reading '$axios')

Solution : Delete $axios an replace with axios, also axios need to be imported as follow. Just add import axios from 'axios' inside <script></script>

7. Problem : error: No Output Directory named "dist" found after the Build completed. You can configure the Output Directory in your Project Settings. Learn More: https://vercel.link/missing-public-directory

Solution : https://medium.com/nerd-for-tech/how-to-deploy-a-nuxt-app-on-vercel-from-github-a7d4e9574ef2

8. Problem : Syntax Error: Unexpected token

Solution : Check each pair of curly brackets in the function.

9. Problem : localStorage is not defined in /pages/dashboard.vue

Solution : https://stackoverflow.com/questions/52474208/react-localstorage-is-not-defined-error-showing

## Special Directories

You can create the following extra directories, some of which have special behaviors. Only `pages` is required; you can delete them if you don't want to use their functionality.

### `assets`

The assets directory contains your uncompiled assets such as Stylus or Sass files, images, or fonts.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `components`

The components directory contains your Vue.js components. Components make up the different parts of your page and can be reused and imported into your pages, layouts and even other components.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `layouts`

Layouts are a great help when you want to change the look and feel of your Nuxt app, whether you want to include a sidebar or have distinct layouts for mobile and desktop.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/layouts).


### `pages`

This directory contains your application views and routes. Nuxt will read all the `*.vue` files inside this directory and setup Vue Router automatically.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/get-started/routing).

### `plugins`

The plugins directory contains JavaScript plugins that you want to run before instantiating the root Vue.js Application. This is the place to add Vue plugins and to inject functions or constants. Every time you need to use `Vue.use()`, you should create a file in `plugins/` and add its path to plugins in `nuxt.config.js`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `static`

This directory contains your static files. Each file inside this directory is mapped to `/`.

Example: `/static/robots.txt` is mapped as `/robots.txt`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/static).

### `store`

This directory contains your Vuex store files. Creating a file in this directory automatically activates Vuex.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/store).

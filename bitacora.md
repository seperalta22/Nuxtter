# twitter clone

## procedimiento

1. instalar nuxt con npm

```bash
pnpm dlx nuxi init <project-name>
```

# Tailwindcss

2. instalar tailwindcss

```bash
pn i -D @nuxtjs/tailwindcss
```

agregar el modulo en nuxt.config.js

```ts
export default {
	modules: ['@nuxtjs/tailwindcss'],
};
```

con eso ya se puede usar tailwindcss pero podemos agregar el archivo tailwind.config.js para configurar tailwindcss

```bash
pnpm dlx tailwindcss init -p
```

3. agregar las configuraciones de tailwindcss en el archivo tailwind.config.js especificas para el proyecto

```ts
module.exports = {
	darkMode: 'class',

	theme: {
		screens: {
			xs: '614px',
			sm: '1002px',
			md: '1022px',
			lg: '1092px',
			xl: '1280px',
		},

		extend: {
			colors: {
				dim: {
					50: '#5F99F7',
					100: '#5F99F7',
					200: '#38444d',
					300: '#202e3a',
					400: '#253341',
					500: '#5F99F7',
					600: '#5F99F7',
					700: '#192734',
					800: '#162d40',
					900: '#15202b',
				},
			},
		},
	},

	plugins: [require('@tailwindcss/forms')],
};
```

# Creacion de componentes por consola con NUXI

4. crear un componente con nuxi

```bash
pn nuxi add component LeftSidebar
```

# Anotaciones Sueltas

1. para hacer una clase dinamica se usa la siguiente sintaxis, que indica que depende de la variable darkMode

```vue
<div :class="{ dark: darkMode }"></div>
```

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

    -mediante la consola se puede crear un componente con el siguiente comando
    -se pueden crear diferentes tipos de componentes como page, layout, component, store, middleware, etc

```bash
pn nuxi add component LeftSidebar
```

-   tambien se pueden crear carpetas dentro de la carpeta components para tener un poco mas de organizacion
    pero a la hora de usar los componentes se debe especificar la ruta completa

ej. components/sidebar/Left.vue se importaria asi

```vue
<template>
	<SidebarLeft />
</template>
```

# Anotaciones Sueltas

1. para hacer una clase dinamica se usa la siguiente sintaxis, que indica que depende de la variable darkMode

```vue
<div :class="{ dark: darkMode }"></div>
```

2. esto se puede hacer en tailwind para ahorrar codigo boilerplate

```vue
<div :class="transition"></div>

<script setup>
const transition = 'transition duration-500 ease-in-out';
</script>
```

3. y por ultimo esto se puede hacer por medio de composable

./composables/useTailwindConfig.ts

```ts
export default () => {
	return {
		defaultTransition: 'transition duration-500 ease-in-out',
	};
};
```

luego en el componente

```vue
<div :class="transition"></div>

<script setup>
const { defaultTransition: transition } = useTailwindConfig();
</script>
```

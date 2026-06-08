# Keysar Cosmetics — Landing Page

## Pendientes (UI/UX)

### Bugs críticos

- [ ] **CTA hover color incorrecto** — `src/components/CTASection.astro:19`
  `hover:bg-[#aa2fbb]` es púrpura, rompe el sistema de color. Cambiar a `hover:bg-[#b08e6e]` o `hover:bg-keysar-dark`.

- [ ] **WhatsApp URL sin código de país** — `src/components/Footer.astro:45`
  `wa.me/5580561135` debería ser `wa.me/525580561135` (igual que en `src/constants/contact.ts`).

### Navegación rota

- [ ] **IDs de sección faltantes** — El navbar enlaza a `#conocenos`, `#servicios`, `#agenda` pero ninguna sección tiene esos `id`. Agregar a los componentes correspondientes.

### Layout

- [ ] **Grid de sucursales** — `src/components/LocationsSection.astro:42`
  3 tarjetas en `md:grid-cols-2` deja la tercera sola en desktop. Cambiar a `md:grid-cols-3` o centrar el huérfano.

### Contenido pendiente

- [ ] **Footer con placeholders** — `src/components/Footer.astro:103-107`
  Reemplazar "WhatsApp pendiente", "Instagram pendiente", "Horario pendiente", "Sucursales por confirmar" con datos reales.

- [ ] **Año de copyright desactualizado** — `src/components/Footer.astro:114`
  `© 2025` → actualizar a año dinámico o 2026.

### Performance / Core Web Vitals

- [ ] **Hero image sin `fetchpriority`** — `src/components/Hero.astro:39`
  Imagen LCP above-the-fold. Agregar `fetchpriority="high"`.

- [ ] **Imágenes sin `width`/`height`** — Hero y logo del Navbar causan layout shift (CLS).
  Declarar dimensiones o usar `aspect-ratio`.

### UX

- [ ] **Menú móvil no se cierra al hacer clic en enlace** — `src/components/Navbar.astro:49`
  `<details>` permanece abierto tras tap en anchor. Agregar script para cerrarlo.

- [ ] **Navbar no sticky** — El header es `absolute` solamente; desaparece al hacer scroll.
  Considerar header sticky con fondo al detectar scroll.

---

# Astro Starter Kit: Basics

```sh
npm create astro@latest -- --template basics
```

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src
│   ├── assets
│   │   └── astro.svg
│   ├── components
│   │   └── Welcome.astro
│   ├── layouts
│   │   └── Layout.astro
│   └── pages
│       └── index.astro
└── package.json
```

To learn more about the folder structure of an Astro project, refer to [our guide on project structure](https://docs.astro.build/en/basics/project-structure/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

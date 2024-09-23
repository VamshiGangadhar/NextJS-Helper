# NextJS-Helper


Create a new Next.js project:
Open your terminal (Command Prompt on Windows, Terminal on macOS) and run the following commands:
```
npx create-next-app@latest young-bot-academy
cd young-bot-academy
```
When prompted, choose the following options:

- Would you like to use TypeScript? › Yes
- Would you like to use ESLint? › Yes
- Would you like to use Tailwind CSS? › Yes
- Would you like to use `src/` directory? › Yes
- Would you like to use App Router? › Yes
- Would you like to customize the default import alias? › No

Install additional dependencies:
In your terminal, run:

```
npm install @radix-ui/react-dialog @radix-ui/react-slot class-variance-authority clsx framer-motion lucide-react tailwind-merge tailwindcss-animate
```

Set up shadcn/ui:
Run the following command to initialize shadcn/ui:

```
npx shadcn-ui@latest init
```

Choose the following options:

- Would you like to use TypeScript (recommended)? › yes
- Which style would you like to use? › Default
- Which color would you like to use as base color? › Slate
- Where is your global CSS file? › › app/globals.css
- Do you want to use CSS variables for colors? › yes
- Where is your tailwind.config.js located? › tailwind.config.js
- Configure the import alias for components: › @/components
- Configure the import alias for utils: › @/lib/utils
- Are you using React Server Components? › yes
- Write configuration to components.json. Proceed? › yes

```
npx shadcn-ui@latest add button
npx shadcn-ui@latest add sheet
npx shadcn-ui@latest add dialog
```

Create the home page component:

- In VS Code, open your project folder
- Create a new file at `app/page.tsx`
- Copy and paste the entire code from the React component we created earlier into this file


Update the layout file:

- Open `app/layout.tsx`
- Replace its contents with the following code:

```
import './globals.css'
import type { Metadata } from 'next'
import { Inter } from 'next/font/google'

const inter = Inter({ subsets: ['latin'] })

export const metadata: Metadata = {
  title: 'Young Bot Academy',
  description: 'Empowering young minds with cutting-edge robotics education',
}

export default function RootLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return (
    <html lang="en">
      <body className={inter.className}>{children}</body>
    </html>
  )
}
```

Start the development server:
In your terminal, run:

```
npm run dev
```

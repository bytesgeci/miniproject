This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

# Faculty Management System (Next.js)

A role-based Faculty Management web application built with **Next.js (App Router)**, **TypeScript**, **Tailwind CSS**, and **shadcn/ui**.  
The system supports multiple user roles such as **Faculty**, **Auditor**, and **Staff Advisor**, each with dedicated dashboards and features.

---

## 🚀 Features

- 🔐 Authentication flow (Login)
- 👨‍🏫 Faculty Dashboard
- 🧾 Course File Management
- 📅 Event Report Management
- 🕵️ Auditor Dashboard
- 👥 Staff Advisor Dashboard
- 🎨 Reusable UI components (Button, Tabs, Dropdowns)
- 🧩 Modular & scalable folder structure
- ⚡ Next.js App Router with layouts and route groups
- 🛡️ Ready for role-based access control via middleware

---

## 🗂️ Project Structure

```txt
src/
├── app/
│   ├── (auth)/                 # Authentication routes
│   │   └── login/
│   │       └── page.tsx
│   │
│   ├── (dashboard)/            # Protected dashboard routes
│   │   ├── layout.tsx          # Dashboard layout (Header + Footer)
│   │   ├── page.tsx            # Dashboard landing page
│   │   │
│   │   ├── faculty/            # Faculty role routes
│   │   │   ├── page.tsx
│   │   │   ├── files/
│   │   │   │   └── page.tsx
│   │   │   └── events/
│   │   │       └── page.tsx
│   │   │
│   │   ├── auditor/            # Auditor role routes
│   │   │   └── page.tsx
│   │   │
│   │   └── staff-advisor/      # Staff Advisor role routes
│   │       └── page.tsx
│   │
│   ├── layout.tsx              # Root layout
│   ├── page.tsx                # Landing / redirect page
│   └── globals.css             # Global styles
│
├── components/
│   ├── layout/                 # App layout components
│   │   ├── Header.tsx
│   │   ├── Footer.tsx
│   │   └── RoleSwitcher.tsx
│   │
│   ├── dashboards/             # Dashboard UI per role
│   │   ├── FacultyDashboard.tsx
│   │   ├── AuditorDashboard.tsx
│   │   └── StaffAdvisorDashboard.tsx
│   │
│   ├── faculty/                # Faculty-specific features
│   │   ├── CourseFileManager.tsx
│   │   └── EventReportManager.tsx
│   │
│   ├── auth/                   # Authentication UI
│   │   └── AuthPage.tsx
│   │
│   └── ui/                     # Reusable UI primitives (shadcn/ui)
│       ├── button.tsx
│       ├── tabs.tsx
│       ├── dropdown-menu.tsx
│       └── sonner.tsx
│
├── hooks/
│   └── useAuth.ts              # Authentication & role state hook
│
├── lib/
│   ├── roles.ts                # Role constants & helpers
│   └── constants.ts            # App-wide constants
│
├── types/
│   └── auth.ts                 # Shared TypeScript types
│
└── middleware.ts               # Role-based route protection


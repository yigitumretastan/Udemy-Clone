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

/udemy-clone
│
├─ /src
│   ├─ /app                      # App Router rotaları
│   │   ├─ layout.tsx            # Root layout (örneğin navbar, footer vs.)
│   │   ├─ loading.tsx           # Genel loading fallback
│   │   ├─ error.tsx             # Global error boundary
│   │   │
│   │   ├─ /home
│   │   │   ├─ page.tsx
│   │   │   └─ ui/                # Home sayfasına ait bileşenler
│   │   │
│   │   ├─ /courses
│   │   │   ├─ layout.tsx         # Courses ile ilgili ortak layout
│   │   │   ├─ page.tsx           # /courses
│   │   │   └─ /[id]
│   │   │       ├─ page.tsx       # /courses/:id (kurs detayı)
│   │   │       └─ ui/             # Kurs detayına özel componentler
│   │   │
│   │   ├─ /auth
│   │   │   ├─ layout.tsx          # Auth işlemlerine özel layout
│   │   │   ├─ login
│   │   │   │   └─ page.tsx        # /auth/login
│   │   │   └─ register
│   │   │       └─ page.tsx        # /auth/register
│   │   │
│   │   ├─ /instructor
│   │   │   ├─ layout.tsx
│   │   │   ├─ dashboard
│   │   │   │   └─ page.tsx
│   │   │   ├─ create-course
│   │   │   │   └─ page.tsx
│   │   │   └─ my-courses
│   │   │       └─ page.tsx
│   │   │
│   │   ├─ /admin
│   │   │   ├─ layout.tsx
│   │   │   ├─ dashboard
│   │   │   │   └─ page.tsx
│   │   │   ├─ users
│   │   │   │   └─ page.tsx
│   │   │   ├─ courses
│   │   │   │   └─ page.tsx
│   │   │   └─ reports
│   │   │       └─ page.tsx
│   │   │
│   │   ├─ /profile
│   │   │   └─ page.tsx
│   │   │
│   │   └─ /cart
│   │       └─ page.tsx
│   │
│   ├─ /_components               # Tüm uygulamada tekrar kullanılan UI bileşenleri (dış rotaya dahil değil)
│   │   ├─ Navbar.tsx
│   │   ├─ Footer.tsx
│   │   ├─ CourseCard.tsx
│   │   └─ Loader.tsx
│   │
│   ├─ /_lib                       # İş mantığı, API çağrıları ve yardımcı fonksiyonlar
│   │   ├─ api.ts
│   │   ├─ auth.ts
│   │   └─ utils.ts
│   │
│   ├─ /_hooks                     # React hook’ları (auth, form, useCourses vs.)
│   │   └─ useAuth.ts
│   │
│   ├─ /_contexts                  # React context’leri (tema, kullanıcı vs.)
│   │   └─ AuthContext.tsx
│   │
│   ├─ /_types                     # TypeScript tipleri
│   │   ├─ user.ts
│   │   ├─ course.ts
│   │   ├─ cart.ts
│   │   └─ auth.ts
│   │
│   ├─ /styles                     # Küresel stil dosyaları
│   │   ├─ globals.css
│   │   └─ tailwind.css (veya başka stil dosyası)
│   │
│   └─ /assets                     # Statik resimler, ikonlar vs.
│       ├─ logo.png
│       └─ favicon.ico
│
├─ next.config.js
├─ tsconfig.json
└─ package.json

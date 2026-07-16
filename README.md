# ✈️ Crazy Vibez Travel

> A full-stack travel-booking web app with real authentication, payments, and media handling — built to production patterns, not a demo.

---

## 🎯 Problem it solves

Booking travel means browsing options, signing in securely, paying, and managing media-rich listings. **Crazy Vibez Travel** delivers that as a single, working full-stack application with the real third-party integrations a production app actually needs — auth, payments, a managed database, and media storage.

---

## ✨ Key Features

- **User authentication** — secure sign-up and login via Clerk.
- **Online payments** — checkout powered by Razorpay.
- **Media management** — image upload and delivery via Cloudinary.
- **Persistent data** — bookings and listings stored in PostgreSQL through Prisma.
- **Modern, responsive UI** — built with Next.js 15 and Tailwind CSS.

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 15 |
| Styling | Tailwind CSS |
| ORM | Prisma |
| Database | PostgreSQL (Neon) |
| Auth | Clerk |
| Payments | Razorpay |
| Media | Cloudinary |

---

## ⚙️ How it works (architecture)

- **Next.js 15** serves both the UI and the API/server logic.
- **Clerk** handles the full auth lifecycle (sign-up, login, sessions).
- **Prisma** models the data and talks to a **PostgreSQL** database hosted on **Neon**.
- **Razorpay** processes payments at checkout.
- **Cloudinary** stores and serves listing images.

```
User ──▶ Next.js 15 (UI + server)
             │
   Clerk (auth) · Razorpay (payments) · Cloudinary (media)
             │
     Prisma ──▶ PostgreSQL (Neon)
```

---

## 🚀 Run it locally

```bash
# 1. Clone and install
git clone https://github.com/eris03/crazy-vibez-travel.git
cd crazy-vibez-travel
npm install

# 2. Create a .env file with your keys
#    DATABASE_URL=your_neon_postgres_url
#    NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=...
#    CLERK_SECRET_KEY=...
#    RAZORPAY_KEY_ID=...
#    RAZORPAY_KEY_SECRET=...
#    CLOUDINARY_URL=...

# 3. Apply the database schema
npx prisma migrate dev

# 4. Start the dev server
npm run dev
```

App runs at `http://localhost:3000`.

---

## 🖼️ Demo / Screenshots

> _Add a live demo link (e.g. a Vercel deployment) and 1–2 screenshots of the booking flow here. For a full-stack app, a clickable live link is the strongest possible signal to a recruiter._

- **Live demo:** `https://YOUR-DEPLOYMENT-URL`
- `![Booking flow](assets/booking-flow.png)`

---

## 🔄️ License

MIT — see [LICENSE](LICENSE).

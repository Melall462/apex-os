# Apex OS

A management platform for a mobile detailing business, built with
React, Supabase, and Vercel.

**Live demo:** https://apex-os-mehar.vercel.app/

## What it does
- Manage customers, with multiple vehicles linked to each customer
- Create jobs by selecting a customer, a vehicle, and a service
- Dashboard comparing this month's revenue against last month's
- Follow-up reminders: customers 60 days past their last completed
  service are flagged, and one click opens a pre-filled email or SMS

## Tech stack
React (Vite), Supabase (PostgreSQL + Auth), Vercel

## Data and security
- Every table has a `user_id` column linked to the authenticated account
- Row-level security policies on all tables ensure users can only read
  and write their own data
- New accounts are seeded with sample data so the demo works immediately

## Run locally
1. `git clone https://github.com/Melall462/apex-os.git`
2. `npm install`
3. Copy `.env.example` to `.env` and add your Supabase URL and anon key
4. `npm run dev`

## Possible improvements
- Scheduled, automatic reminders using a Supabase edge function
- Database-generated IDs instead of client-generated ones
- Automated tests

# Next.js 15 App Router: Default Export in Page Component Fails Silently in Production

This repository demonstrates a subtle bug in Next.js 15's App Router when using a default export in a page component. The issue only manifests in production builds.

## Bug Description

A simple page component with a default export works correctly in development mode.  However, when building for production, the page fails to render without any errors in the console.  This makes debugging extremely difficult.

## Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev` (Development mode: Works as expected)
4. Run `npm run build && npm run start` (Production mode: Fails silently)

## Solution

The solution involves changing the default export to a named export.  This resolves the issue, and the page renders correctly in both development and production.
# SvelteKit Vite 4.2 SSR error

## With Vite 4.2
```typescript
npm i
npm run dev
```

An `Internal server error: window is not defined` error is thrown.

## With Vite 4.1
Replace the vite version in `package.json` with `4.1.4` (the last release before `4.2.0`) and repeat the above steps. The site will load without issue.

## Notes

I realise that this is perhaps a little niche, and I am not enitrely sure where in the chain this issue will exist, but this doesn't strike me as correct behaviour.

The guard against rendering anything on the server is deliberate for a specific use case I have for Safari. I only need to SSR in dev because of this issue: https://github.com/sveltejs/kit/issues/7805.

# ✅ Vercel Deployment Checklist

## Pre-Deployment Steps

- [ ] Project code committed to GitHub
- [ ] Vercel account created (https://vercel.com)
- [ ] GitHub connected to Vercel
- [ ] .env file **NOT** committed (add to .gitignore)
- [ ] package.json has "start" script
- [ ] vercel.json configured
- [ ] Database credentials ready

## Database Setup

- [ ] Database created (PlanetScale, Supabase, or existing)
- [ ] Connection credentials obtained:
  - [ ] DB_HOST
  - [ ] DB_USER
  - [ ] DB_PASSWORD
  - [ ] DB_NAME
  - [ ] DB_PORT

## Vercel Deployment

### Option A: Dashboard Method
1. [ ] Go to https://vercel.com/dashboard
2. [ ] Click "Add New" → "Project"
3. [ ] Select GitHub repository
4. [ ] Import project
5. [ ] Add Environment Variables:
   - [ ] DB_HOST
   - [ ] DB_NAME
   - [ ] DB_USER
   - [ ] DB_PASSWORD
   - [ ] DB_PORT
   - [ ] JWT_SECRET = `eduCore_secure_jwt_secret_2026_@!`
   - [ ] ADMIN_USERNAME = `Apexiums@school.com`
   - [ ] ADMIN_PASSWORD = `Apexiums1717`
6. [ ] Click "Deploy"
7. [ ] Wait for deployment to complete

### Option B: CLI Method
1. [ ] Install Vercel CLI: `npm install -g vercel`
2. [ ] Login: `vercel login`
3. [ ] Deploy: `vercel`
4. [ ] Add environment variables: `vercel env add [VAR_NAME]`
5. [ ] Production deploy: `vercel --prod`

## Post-Deployment Testing

- [ ] Frontend loads at https://your-project.vercel.app
- [ ] Login page appears
- [ ] Admin login works:
  - Email: `Apexiums@school.com`
  - Password: `Apexiums1717`
- [ ] Dashboard accessible after login
- [ ] Navigation between pages works
- [ ] Logout button present and functional
- [ ] Database operations working (if DB connected)
- [ ] No console errors in browser dev tools
- [ ] API calls return data

## Security Verification

- [ ] HTTPS enabled (default on Vercel)
- [ ] Environment variables not exposed
- [ ] Admin credentials changed (recommended)
- [ ] Database access restricted to Vercel IPs only
- [ ] JWT_SECRET is strong and unique

## After Deployment

- [ ] Add custom domain (Optional)
- [ ] Set up analytics (Optional)
- [ ] Configure auto-deploys on git push
- [ ] Set up error monitoring
- [ ] Share project URL with team

## Troubleshooting

If deployment fails:
1. Check Vercel build logs
2. Verify all environment variables are set
3. Test locally: `npm run start`
4. Check database connectivity
5. Review error messages in console

---

**Status**: Ready for Deployment ✅

Your project is configured and ready to deploy to Vercel!

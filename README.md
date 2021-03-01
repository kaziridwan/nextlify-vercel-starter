# README
This is a static CMS written in nextjs and netlify-cms, using netlify's git-gateway.
The goals of this project are:
1. To create a zero-fee CMS template
2. To be based off of completely opensource solutions, and no vendor lock-in

# Quickstart
1. Deploy to vercel

    [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https://github.com/kaziridwan/nextlify-vercel-starter)

2. Copy your vercel app url from vercel dashboard, and github repo address
3. Configure netlify-cms config

    goto `public/admin/config.yml`
      ```
          backend:
            name: github
            repo: OWNER/YOUR_GITHUB_REPO
            base_url: https://example.com/
            auth_endpoint: api/auth

      ```
4. [Set up netlify-cms oauth](https://www.npmjs.com/package/@openlab/vercel-netlify-cms-github)
   1. Create a GitHub OAuth application
      1. Go to https://github.com/settings/developers.
      2. Set Homepage URL to your site's homepage
      3. Set Authorization callback URL to `https://YOUR_SITE_HERE/api/callback
      4. Make a note of your client_id and client_secret
   2. Setup Vercel environment variables
      1. Go to your vercel dashboard, https://vercel.com
      2. Navigate to your project then Settings > Environment Variables
      3. Add OAUTH_CLIENT_ID and set the value from the GitHub OAuth application
      4. Add OAUTH_CLIENT_SECRET and set the value from the GitHub OAuth application
      5. You can store them however you like but secrets should be the most secure
      6. Make sure your environment variables are exposed on the deployment(s) you need

---

# Where are we right now and what are the implications?
## No fee
We have been able to achieve a complete zero-fee system, with two lock-ins
1. netlify identity
2. github lock-in

## Completion of basic principles
1. remove dependancy on oauth
   1. use vercel
      1. https://github.com/robinpokorny/netlify-cms-now
2. remove github lock-in
   1. store it in gitlab
      1. you loose codespaces for private repos
         1. add in docker

## Roadmap
- create a nextjs static site
  <!-- - on gitlab -->
  - on github
- move over to vercel
  - deploy on vercel
- add netlify-cms
  - add pages and collections
    - home
      - navigation
        - links[]
      - heroImage
      - heroCTA
      - heroText
      - Sections
      - footer
        - col[]
          - title
          - links[]
    - about
      - herosection
      - heroImage
    - contact
      - herosection
      - heroImage
    - blog[]
  <!-- - add gitlab oauth to vercel -->
  - add github oauth to vercel
    - https://github.com/robinpokorny/netlify-cms-now
- add docker, docker-compose and scripts
  - make a dockedrepo
  - make it a monorepo
- move to gitlab
- add tinacms
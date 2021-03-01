# README
This is a static CMS written in nextjs and netlify-cms, using netlify's git-gateway.
The goals of this project are:
1. To create a zero-fee CMS template
2. To be based off of completely opensource solutions, and no vendor lock-in

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
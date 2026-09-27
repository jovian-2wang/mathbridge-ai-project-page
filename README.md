# MathBridge AI project page

This is a public-facing, static project page for MathBridge AI, based on [Roman Hauksson-Neill's academic project Astro template](https://github.com/RomanHauksson/academic-project-astro-template). It describes the prototype and the [NSF FINDERS Foundry planning award #2627693](https://www.nsf.gov/awardsearch/show-award/?AWD_ID=2627693). It does not contain MathBridge's private application source, credentials, student records, or application backend.

## Run locally

Requires Node.js 24 or newer.

```bash
cd mathbridge-ai-project-page
npm ci
npm run dev
```

Open http://localhost:4321 in a browser. Run npm run build to regenerate dist/. If the extracted folder has another name, cd into the folder containing package.json.

Edit public copy in src/paper.mdx, the interactive unit-rate illustration in src/components/LearningLab.astro, the live app guide in src/components/DemoNavigator.astro, the technical figure in src/components/Architecture.astro, and styling in src/styles/mathbridge.css. Institutional marks are in public/brands/.

The unit-rate illustration uses fixed questions and fixed feedback; it is labeled as an illustration and does not call the private tutor. The running application is embedded separately, with a new-tab fallback. A role-specific test account is required to sign in. Selecting a role in the guide does not change the signed-in role in the application.

## Publish separately from the private app

Create a **separate repository** from these files for the public page. In GitHub, enable Pages with **GitHub Actions** as the source. The included `.github/workflows/astro.yml` builds and deploys the static page on a push to `main`, including for a repository subpath. Your MathBridge AI application repository can stay private. Do not copy its `.env`, database exports, or private source into this project-page repository.

The page links to the existing MathBridge platform at `https://mathbridge-ai.duckdns.org/`. Its Code button points to the private repository and is labeled accordingly; visitors need repository access. Check that the live platform and its login experience are ready for external visitors before sharing the project page.

## Institutional identities and project description

The [NSF project record](https://nsf.elsevierpure.com/en/projects/nsf-ff-planning-a-student-aware-ai-platform-for-connected-and-con/) names UT San Antonio as lead and the University of Florida as a sub-awardee. The marks in this page come from the universities' official websites, and they appear in separate institutional panels with their roles. Confirm use of both marks with the project and university brand contacts before public launch. UF's [brand guidance](https://brandcenter.ufl.edu/the-university-logo/) includes restrictions on pairing marks; UT San Antonio's [brand toolkit](https://www.utsa.edu/marcomstudio/resources/brand-toolkit/logos/) provides current logo guidance. Do not recolor or modify the supplied files.

The prototype copy was cross-checked against a September 25, 2026 MathBridge AI source snapshot and the user-supplied visual progression and diagnosis document. The student preference fields in the source snapshot are language, up to three interests, and optional automatic read-aloud. The Answer Edition extraction process and `curriculum_instructional_supports` table shown in the diagram are a proposed extension, not part of the inspected runtime. The wider K–12 aim is described as a research vision; current coverage is described as selected Grade 6 topics. Review the live product and all claims before publishing.

## Credits

The page is adapted from Roman Hauksson-Neill's [Academic Project Page Template](https://github.com/RomanHauksson/academic-project-astro-template), itself adapted from earlier academic project pages. The source template identifies its license as [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Retain the template credit in the site footer and comply with the license if distributing this adaptation. University marks remain the property of their respective institutions.

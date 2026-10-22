# Technology deck and source artwork

The profile displays **24 local SVG tiles** in [tiles/](tiles/), each with a 54 × 54 viewBox, a rounded graphite background, a muted cyan border and a centered 38 × 38 artwork canvas. Scaling is uniform in both directions. Native inline images wrap naturally; the README uses no custom CSS, JavaScript or external icon service. GitHub's level-two heading supplies the thin divider beneath `// tech_deck`.

Every tile has a title, description and README alt text. The utility drawer includes a readable deck index so the section remains usable when images fail. Original artwork colours are preserved; only upstream neutral `#242938` container rectangles are removed. Coloured source backgrounds remain intact inside the uniform outer tile. Terminal pills use GitHub's native code styling, adapting to light and dark themes.

Pills use native nonbreaking spaces and, for scikit-learn, a nonbreaking hyphen so each name stays intact on narrow screens. Local browser checks cover both themes at 1280 and 360 px: 13 + 11 desktop tiles, 5 + 5 + 5 + 5 + 4 mobile tiles, no horizontal overflow with the drawer closed or open, and readable fallback text with icon requests blocked. These previews approximate GitHub; GitHub remains the final renderer.

The earlier 35 labelled badge files remain here as local source artwork; they are no longer embedded in the README. Twenty-five contain Skill Icons artwork and ten are text-only. Keeping them preserves the source and avoids deleting existing local work during review. The displayed deck adds 63,797 bytes; no extra network requests are needed.

## Display inventory

- Main deck (24): HTML, CSS, JavaScript, TypeScript, Python, C++, Dart, React, Flutter, FastAPI, Vite, Tailwind CSS, Node.js, Express.js, MongoDB, Firebase, PostgreSQL, Supabase, Docker, Nginx, Vercel, Git, GitHub, Azure.
- Text pills (13): Gemini API, MediaPipe, SQLAlchemy, Alembic, WebSockets, MLflow, scikit-learn, Apps Script, JWT/RBAC, REST APIs, Google Sheets, WhatsApp workflows, UPI workflows.
- Utility drawer (17): Zustand, React Router, Mongoose, Firestore, Firebase Authentication, PWA, Web Speech API, Responsive design, Pytest, Ruff, Playwright, GitHub Actions, Render, PostgreSQL TLS/RLS, Tool calling, Explainable AI (reference-based), Model calibration.

All 35 technologies from the previous section remain represented. Existing lower-priority items move to native text, with verified APIs, tools and concepts added. Presence denotes implementation evidence, not a proficiency ranking or a guarantee that a hosted provider is available.

## Artwork provenance

Skill Icons source: [tandpfun/skill-icons](https://github.com/tandpfun/skill-icons), pinned to [`7f7e691`](https://github.com/tandpfun/skill-icons/commit/7f7e691e71aec64e8354bf697835e009d1ad80f8). The complete MIT notice is retained in [LICENSE.skill-icons.txt](LICENSE.skill-icons.txt). Logo paths and proportions are retained in the tiles. Firebase's upstream artwork includes two embedded PNG layers; these remain self-contained inside its SVG and make no external requests. Source inventory:

| Badge | Upstream artwork |
| --- | --- |
| [C++](cpp.svg) | [CPP.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/CPP.svg) |
| [Python](python.svg) | [Python-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Python-Dark.svg) |
| [JavaScript](javascript.svg) | [JavaScript.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/JavaScript.svg) |
| [TypeScript](typescript.svg) | [TypeScript.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/TypeScript.svg) |
| [Dart](dart.svg) | [Dart-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Dart-Dark.svg) |
| [HTML](html.svg) | [HTML.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/HTML.svg) |
| [CSS](css.svg) | [CSS.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/CSS.svg) |
| [FastAPI](fastapi.svg) | [FastAPI.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/FastAPI.svg) |
| [Node.js](nodejs.svg) | [NodeJS-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/NodeJS-Dark.svg) |
| [Express.js](express.svg) | [ExpressJS-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/ExpressJS-Dark.svg) |
| [PostgreSQL](postgresql.svg) | [PostgreSQL-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/PostgreSQL-Dark.svg) |
| [Supabase](supabase.svg) | [Supabase-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Supabase-Dark.svg) |
| [MongoDB](mongodb.svg) | [MongoDB.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/MongoDB.svg) |
| [Firebase](firebase.svg) | [Firebase-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Firebase-Dark.svg) |
| [SQLAlchemy](sqlalchemy.svg) | Text label; no logo substituted |
| [Alembic](alembic.svg) | Text label; no logo substituted |
| [WebSockets](websockets.svg) | Text label; no logo substituted |
| [React](react.svg) | [React-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/React-Dark.svg) |
| [Flutter](flutter.svg) | [Flutter-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Flutter-Dark.svg) |
| [Vite](vite.svg) | [Vite-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Vite-Dark.svg) |
| [Tailwind CSS](tailwind.svg) | [TailwindCSS-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/TailwindCSS-Dark.svg) |
| [Zustand](zustand.svg) | Text label; no logo substituted |
| [React Router](react-router.svg) | Text label; no logo substituted |
| [Gemini API](gemini.svg) | Text label; no logo substituted |
| [MediaPipe](mediapipe.svg) | Text label; no logo substituted |
| [scikit-learn](scikit-learn.svg) | [ScikitLearn-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/ScikitLearn-Dark.svg) |
| [MLflow](mlflow.svg) | Text label; no logo substituted |
| [Apps Script](apps-script.svg) | Text label; no logo substituted |
| [Docker](docker.svg) | [Docker.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Docker.svg) |
| [Nginx](nginx.svg) | [Nginx.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Nginx.svg) |
| [Azure](azure.svg) | [Azure-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Azure-Dark.svg) |
| [Vercel](vercel.svg) | [Vercel-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Vercel-Dark.svg) |
| [Render](render.svg) | Text label; no logo substituted |
| [Git](git.svg) | [Git.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Git.svg) |
| [GitHub](github.svg) | [Github-Dark.svg](https://github.com/tandpfun/skill-icons/blob/7f7e691e71aec64e8354bf697835e009d1ad80f8/icons/Github-Dark.svg) |

## Source verification

| Group | Evidence |
| --- | --- |
| Languages | C++: public `Ameya5006/neetcode-submissions` binary-search `.cpp` source, plus local algorithm source. Python: Aletheia and SAHAY backend source. JavaScript/TypeScript/HTML/CSS: PalmChef/GymFlow/portfolio implementation and manifests. Dart: Amedic and FloatChat source. |
| Backend and Data | SAHAY backend requirements and imports establish FastAPI, SQLAlchemy, Alembic, Supabase/PostgreSQL and WebSockets. PalmChef's server imports Express and Mongoose/MongoDB. GymFlow implements Firebase Auth and Firestore. |
| Web and Mobile | PalmChef/GymFlow/Aletheia manifests and implementation establish React, Vite, Tailwind CSS, Zustand and React Router. Amedic/FloatChat pubspec and Dart source establish Flutter. |
| AI, APIs and Infrastructure | PalmChef has Gemini API and MediaPipe implementation. Aletheia uses scikit-learn and MLflow, Docker/NGINX deployment and Azure workflows. GymFlow uses Apps Script. GymFlow Vercel configuration and public deployment; PalmChef's documented Render interface; Git history and GitHub remotes/workflows. |

Project repository links and precise implementation notes are in the local `docs/profile-audit.md`; the README links all six projects. C++ source: [binary-search submission](https://github.com/Ameya5006/neetcode-submissions/blob/main/Data%20Structures%20%26%20Algorithms/binary-search/submission-0.cpp).

## Selection

The 24 main tiles prioritize recognizable technologies. scikit-learn is now a text pill; Zustand, React Router and Render move into the utility drawer. No previously displayed technology is removed.

New concept/tool labels were checked in actual source: SAHAY's `app/core/security.py`, API routes, `app/core/config.py` encrypted PostgreSQL URL validation and RLS-enabling Alembic migration; Aletheia's `pyproject.toml` (Pytest/Ruff), frontend manifest and browser tests (Playwright), Azure GitHub workflow and implemented calibration/reference explanations; PalmChef's Mongoose/Zustand/router imports, manifest/service-worker registration, browser speech implementation, responsive component classes and Gemini tool-call execution; GymFlow's Firebase auth/Firestore imports, `SpreadsheetApp`, WhatsApp links and UPI URI builder. TLS/RLS describes implemented configuration and migration, not a claim about public database policy access. Explainable AI is explicitly qualified as reference-based and noncausal in the project description. Tool calling is implemented; deployment status remains qualified above in the profile.

Omitted: Java (only generated Flutter plugin Java files verified; no independently authored Java work), Google Sheets API (the integration uses Apps Script `SpreadsheetApp`), VS Code (optional editor tile would crowd the 24-item deck), and a standalone offline-support claim (PalmChef's worker references `/logo.png`, absent from the inspected public assets; end-to-end offline behaviour was not verified). PWA remains as the verified manifest/worker implementation, without claiming a successful offline session.


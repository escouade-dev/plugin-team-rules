# Team rules · plugin for Escouade

Allows or denies the agents’ commands by the team’s rules, written in `rules.json`. A TypeScript program answering `permissions/decide`; a refusal tells the agent why.

Edit `rules.json`: `deny` and `allow` hold command prefixes, or `{ "command", "message" }` for a refusal with its own message. Escouade runs `dist/plugin.mjs` with Node.

> Autorise ou refuse les commandes des agents selon les règles de l’équipe, écrites dans `rules.json`. Un programme TypeScript qui répond à `permissions/decide` ; un refus dit sa raison à l’agent.

One of the example plugins of [Escouade](https://escouade.dev) (id `dev.exemple.team-rules`), published on its store: https://store.escouade.dev. The documentation shows it whole: https://escouade.dev/en/docs/plugins/examples

## Develop

```sh
npm install
npm test            # against the fake Escouade of @escouade-dev/plugin
npm run build       # dist/plugin.mjs, the file Escouade runs (committed)
npm run validate    # escouade-plugin validate .
npm run bench       # Escouade's conformance bench
```

## Try it in Escouade

Plugins view › “In development”, then this folder; or install it from the store.

## License

MIT (`LICENSE`).

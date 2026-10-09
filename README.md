# muxel-library-example

An example **team library** for muxel. It contains a single
`muxel-library.toml` with two snippets, two runners and two loops you can use to try out shared libraries.

## Add it in muxel

1. Open **Settings → Libraries → Add library**.
2. Paste the URL:

   ```
   https://github.com/freddysae0/muxel-library-example.git
   ```

muxel clones the repo and shows its snippets, runners and loops alongside your own.

## File format

`muxel-library.toml` has three kinds of entries:

- `[[snippets]]` — reusable text (`name`, `text`, `submit` to send it right away).
- `[[runners]]` — a prompt run in a terminal (`name`, `prompt`, optional `preset`; `{{input}}` is replaced with your input).
- `[[loops]]` — a prompt run on a `schedule` (`every_hours` or `daily_at`), with `post_run` = `leave` or `exit`.

`preset` is optional; if omitted, the **Current** preset is used. Shared loops arrive **switched off** —
enable them yourself once you've reviewed them.

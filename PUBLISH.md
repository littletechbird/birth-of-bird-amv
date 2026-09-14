# Publish — littletechbird/birth-of-bird-amv

Exact commands to create and push this **public** documentation pack.

Docs + LICENSE only. Do **not** add binary video/audio.

---

## Prerequisites

- `gh` authenticated as a user that can create repos under **littletechbird**
- Working tree at `/workspace/birth-of-bird-amv` (or a clone of this pack)
- Public scrub already applied (no real human surname, no private device names, no secrets/emails/phones/addresses)

---

## One-shot (init + create + push)

```bash
cd /workspace/birth-of-bird-amv && \
git init && \
git add . && \
git -c user.email='hatch@littletechbird.local' -c user.name='Hatch' \
  commit -m 'Birth of Bird — public forever AMV craft pack' && \
gh repo create littletechbird/birth-of-bird-amv \
  --public \
  --source=. \
  --remote=origin \
  --push \
  --description 'Birth of Bird — ~7min anthem AMV craft pack (story circle, process, lyrics; free forever)'
```

Expected remote after success:

**https://github.com/littletechbird/birth-of-bird-amv**

---

## If the repo already exists

```bash
cd /workspace/birth-of-bird-amv
git init
git add .
git -c user.email='hatch@littletechbird.local' -c user.name='Hatch' \
  commit -m 'Birth of Bird — public forever AMV craft pack'
git branch -M main
git remote add origin https://github.com/littletechbird/birth-of-bird-amv.git
git push -u origin main
```

(If `origin` already exists, use `git push -u origin main` only.)

---

## If `gh auth` fails

1. Leave the pack on disk at `/workspace/birth-of-bird-amv`.
2. Authenticate on the local device (`gh auth login`) as the littletechbird maintainer.
3. Re-run the one-shot (or the “already exists” path).

Do not embed tokens in this repo. Do not paste API keys into docs.

---

## Post-push checklist

- [ ] Repo is **public**
- [ ] README renders with Watch table, Hatch template, sister guides, free forever / not for kids
- [ ] No binaries accidentally added (`git ls-files` should be markdown/LICENSE only)
- [ ] Scrub grep clean (no private surnames, emails, private paths, API keys)
- [ ] Optional: update TBD YouTube / X URLs in README + LINKS when live
- [ ] Optional: reply on the X proof post with the GitHub URL when that post ships

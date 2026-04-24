# contributing to solstice os

so you want to help build solstice? cool. here's how.

## making an overlay (the main way people contribute)

the whole point of solstice is that overlays are decentralized. you make one, you share it, people use it. no gatekeeping, no approval process.

### what an overlay looks like

create a github repo. that's it. structure it like this:

```
your-overlay/
├── recipes/
│   ├── package1.sh
│   ├── package2.sh
│   └── ...
├── README.md
└── metadata.yml (optional)
```

pretty straightforward.

### test it locally

before you share it, test it:

```bash
solpm add-overlay /path/to/your-overlay
solpm install package1
```

does it work? cool, ship it.

### share it with the world

push to github and share the url:

```bash
solpm add-overlay https://github.com/yourname/your-overlay
```

people can now use your overlay. that's it. you're done.

## how to write recipes

see [RECIPE_SPEC.md](docs/RECIPE_SPEC.md) for the detailed spec and examples. but basically it's just bash scripts that compile and install packages.

## installing solstice with overlays

when someone's installing solstice, they can just do:

```bash
solstice-install --enable-recommended
```

this automatically adds the recommended overlays:
- **solstice-gaming** — proton, wine, games
- **solstice-nvidia** — nvidia driver recipes
- **solstice-dev** — dev tools, languages
- **solstice-multimedia** — ffmpeg, media stuff

or they can add overlays manually anytime:

```bash
solpm add-overlay https://github.com/user/my-overlay
```

## annual awards

every year we do this thing where the community votes on the best overlays. winners get:
- featured on solstice-os.org
- mentioned in the release notes
- community recognition

we're not gatekeeping winners or anything. just celebrating people who made cool stuff. and yeah, you still manually add them, we're not forcing anything.

## contributing to core recipes

want to improve the core distro itself? yeah, we take pull requests.

- find a bug? file an issue.
- got a fix? send a pr.
- improved documentation? we'll merge it.
- you'll get credited.

## just be cool about it

- be nice to people
- don't be a gatekeeper
- credit people who help you
- help newer people learn
- it's open source, we're all here because we like this stuff

that's it. build cool overlays, contribute when you feel like it, hang out in the community. we're all learning together.

## shoutouts

- **claude** — helped design the whole community overlay system so it actually works
- **NEOAPPS** — early collaborator, distro developer, helping with package manager architecture
- **ImAmir** — system architecture design contributions
- **linux from scratch** — the inspiration for how we approach bootstrapping

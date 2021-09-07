# lnkds

Scrapp all informations you whant of linkedIn profile's.

```bash
$ lnkds --help

lnkds 0.1.2

Teddy F. <pro@teddyfontaine.fr>

This doc string acts as a help message when the user runs '--help' as do all doc strings on fields

USAGE:
    lnkds [FLAGS] <LI_AT> <SUBCOMMAND>

ARGS:
    <LI_AT>    "li_at" from LinkedIn Cookie

FLAGS:
    -h, --help       Print help information
    -v, --verbose    A level of verbosity, and can be used multiple times
    -V, --version    Print version information

SUBCOMMANDS:
    help       Print this message or the help of the given subcommand(s)
    profile    A subcommand to Get LinkedIn profile (basic informations, experiences,
               certificates, ...)
```

## lnkds-profile

```bash
$ lnkds <AQE...> profile <tf...> --help

lnkds-profile

A subcommand to Get LinkedIn profile (basic informations, experiences, certificates, ...)

USAGE:
    lnkds <LI_AT> profile <USER>

ARGS:
    <USER>    User account you whant to parse

FLAGS:
    -h, --help       Print help information
    -V, --version    Print version information
```

## Parsing rules

- Experiences: `"$type": "com.linkedin.voyager.dash.identity.profile.Position"`
- Experiences_groups: `"$type": "com.linkedin.voyager.dash.identity.profile.PositionGroup"`
- Medias: `"$type": "com.linkedin.voyager.dash.identity.profile.treasury.TreasuryMedia"`
- Profile: `"publicIdentifier": "teddyfontaine"` + `"$type": "com.linkedin.voyager.dash.identity.profile.Profile"`
- Educations: `"$type": "com.linkedin.voyager.dash.identity.profile.Education"`
- Certifications: `"$type": "com.linkedin.voyager.dash.identity.profile.Certification"`
- Skills: `"$type": "com.linkedin.voyager.dash.identity.profile.Skill"`
- Projects: `"$type": "com.linkedin.voyager.dash.identity.profile.Project"`
- Organizations: `"$type": "com.linkedin.voyager.dash.identity.profile.Organization"`

## Realase

This project support `@release-it` with 2 plugins `@release-it/keep-a-changelog` and `@release-it/bumper`.

- [@release-it](https://github.com/release-it/release-it)
- [@release-it/keep-a-changelog](https://github.com/release-it/keep-a-changelog)
- [@release-it/bumper](https://github.com/release-it/bumper)

```bash
$ sudo npm install -g release-it
$ sudo npm install -g @release-it/keep-a-changelog
$ sudo npm install -g 
```

## Voyager api limitations

- This api can't getted over 18 experiences.

## Todos

- [x] Implementation of user experiences
- [ ] Implementation of user experiences by groups
- [ ] Implementation of experiences medias
- [ ] Implementation of user profile
- [ ] Implementation of user educations
- [ ] Implementation of user certifications
- [ ] Implementation of user skills
- [ ] Implementation of user projects
- [ ] Implementation of user organizations
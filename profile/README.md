# Welcome to the OBD database (OBDb)

The OBD database is an open source community effort to document the diagnostic parameters and codes (DTCs) that can be used to talk to cars.

## Getting involved

Browsing the database doesn't require any kind of account, but if you want to contribute then you'll need a GitHub account ([signing up is easy!](https://github.com/signup)).

The OBDb is organized around vehicle makes and models. If there isn't yet [a repository](https://github.com/orgs/OBDb/repositories) for your vehicle's make and model, please [request it](https://github.com/OBDb/meta/issues/new?assignees=jverkoey&labels=new-vehicle&projects=&template=new-make-and-model.md&title=%5Bmake%5D+model).

## Repository structure

Each vehicle repo's directory is organized as follows:

```plaintext
signalsets/
  └── v3/
      ├── default.json        # Default configuration
      └── 2012-2020.json      # Example override configuration for specific years
```

- **default.json**: Acts as the primary configuration file. This file is the default fallback for any years not specified by an override file.

- **2012-2020.json**: A specific configuration override for model years 2012-2020, differentiating these years from the baseline configuration in `default.json`.

If a new generation is introduced in the future, a new JSON file (e.g., `2021-2027.json`) can be created to lock in the second-generation configuration, allowing `default.json` to reflect the latest specifications.

## Copyrights

The text of the OBDb is copyrighted (automatically, under the Berne Convention) by OBDb editors and contributors and is formally licensed to
the public under one or several liberal licenses. Most of OBDb's text is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License ([CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)).

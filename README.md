# retro-weekly

This repository is a template that can be cloned 1:1 (with some slight alterations of configurations) to generate weekly retros for your GitHub organization or for a specific user. It imlements [retrogen](https://github.com/cutenode/retrogen), so if you care about the underlying JavaScript you should look there.

# Usage

You've got two options:

- Use this repostiory as a tempalte repository for your own project.
- Use the code in this repostiory as "inspiration" for your own implementation of retrogen.

To make this work for your organization, you'll need to change one thing and might want to change a few others:

- You'll **need** to change the "organization" variable in `generate.js` to your organization's GitHub name. This can also be a username.
- You have the option to change the date range in `generate.js` to something more appropriate for your organization. This is simply the Luxon `DateTime` API. See [the #minus](https://moment.github.io/luxon/api-docs/index.html#datetimeminus) docs for more information.
  - If you do change this, you'll also want to update the cron settings in [`run.yml`](./.github/workflows/run.yml).
- You have the option to change some of the configuration around the generated PR in [`run.yml`](./.github/workflows/run.yml)
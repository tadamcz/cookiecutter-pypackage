{% if cookiecutter.dokku == 'y' -%}
# Deployment
First deploy:
1. Install the official Dokku cli `brew install dokku/repo/dokku`
2. Set the `DOKKU_HOST` environment variable (can be an IP address or a named host defined in your `~/.ssh/config`)
3. `dokku --app {{cookiecutter.project_slug.replace('_','-')}} apps:create`

Subsequent deploys:
1. `git push dokku`

Dokku configuration is read from:
- `Procfile`
- `.buildpacks`
- `app.json`
{%- endif %}

# Awesome Foundation hits $2 million in grants!

Our little microsite to celebrate.

## Updating the projects

Copy the content from the YAML column in the [projects
spreadsheet](https://docs.google.com/spreadsheets/d/14qiEDDmgJ53VJ0UVm-_LlOnTFWoOTxA5bBJQfeegYuA/edit#gid=0), paste the values in to `public/_data/projects.yml`, and remove all the `"`s that Google annoyingly inserts. (Hopefully no projects have `"`s in their names or descriptions, otherwise you'll need to manually tweak them.)

## Local setup

### Docker

*Cedric to fill out*

### Local

If you don't have Docker set up but have a Mac, you can still run the site. Open up a terminal, navigate to the
directory, and run:

```
bundle install
bundle exec rake run_app
```

Then navigate to http://localhost:4000.

Ruby should be installed on your machine already, but if not, you should use the Docker
instructions.

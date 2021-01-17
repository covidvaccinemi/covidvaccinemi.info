## Updating data

Edit `data/vaccine-availability.json` with this format...

```
{
  "data": [
    [
      "<a href='https://www.washtenaw.org/3269/COVID-19-Vaccination'>Washtenaw</a>",
      "No",
      "2021/01/14"
    ],
    [
      "<a href='https://www.waynecounty.com/covid19/covid-19-vaccine-information.aspx'>Wanye</a>",
      "No",
      "2021/01/15"
    ],
    [
      "Foo",
      "No",
      "2021/01/15"
    ]
  ]
}
```

## Local development

Set up

```
gem install bundler jekyll
bundle install
```

Run local server

```
bundle exec jekyll serve
```

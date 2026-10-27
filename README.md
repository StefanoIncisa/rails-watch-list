# Rails Watch List

A movie watch list app built with **Ruby on Rails** and **PostgreSQL**. The goal is to let users create themed lists (for example "Classic thrillers") and bookmark movies into them with a short comment.

Built during the [Le Wagon](https://www.lewagon.com) AI Software Development bootcamp (2026).

> Status: work in progress. The project is set up (Rails 8, PostgreSQL, Bootstrap, Simple Form, RSpec) and the models and pages are the next step.

## Planned data model

```
Movie  1 ──< Bookmark >── 1  List
title, overview,      comment     name
poster_url, rating
```

- A list has many bookmarks and many movies through bookmarks
- A movie can be in many lists, and cannot be deleted while it is bookmarked
- The same movie can only be bookmarked once per list

## Tech stack

| Layer | Technology |
| --- | --- |
| Framework | Ruby on Rails 8 |
| Database | PostgreSQL |
| Front end | Bootstrap 5, Simple Form, Font Awesome |
| Testing | RSpec |

## Run it locally

```bash
git clone https://github.com/StefanoIncisa/rails-watch-list.git
cd rails-watch-list
bundle install
rails db:create db:migrate
rails server
```

## Roadmap

- [ ] Movie, List and Bookmark models with validations
- [ ] Seed movies from an external movie API
- [ ] Pages to create lists and add bookmarks
- [ ] Deploy

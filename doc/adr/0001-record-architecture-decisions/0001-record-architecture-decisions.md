# ADR-0001 - Record architecture decisions

## Date

2018-12-27

## Status

Accepted

## Context

Most projects suffer from a common problem : they usually don't keep a clear history of all the architectural decisions if the project.

It might not appear as an issue at first but as the project evolves it becomes less and less clear why each change was made,
leading to somewhat wrong decisions : should we change existing code and take the risk of breaking the application because
we might have missed an important decision, or should we keep it (fearing we might break something) and take the risk of 
paralyzing the project with an accumulation of potentially wrongly-kept decisions and changes ?

To avoid this dilemna it appears we have to do something to keep a record of all architectural decisions. 

## Decision

We will start using Lightweight Architecture Decision Records (further refered as ADR) as explained 
[here](https://blog.stack-labs.com/code/adr-to-remember-past-archiectural-decisions/#format-d-un-adr) 
or [here](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions).

Here are a few hints of how we will use ADRs :

* We will keep all ADRs in a Git respository so they can be versioned
* We will materialize Each ADR as a separate file within the repository
* We will prefix each ADR by an ordered number (0001 to 9999), and keep ADRs numbers sequential
* We will keep each ADR as short as possible, trying to limit ourselves to 1-2 pages max
* We will use Markdown as the template engine of our ADRs
* We will always keep ALL written ADRs but we will mark old ADRs as superseded if they are

The markdown format we will use when writing an ADR is the following :

```markdown
# Title: These documents have names that are short noun phrases. For example, "ADR-0001 - Deployment on Ruby on Rails 3.0.10" or "ADR 9: LDAP for Multitenant Integration"

## Date

YYYY-MM-DD

## Status

A decision may be "proposed" if the project stakeholders haven't agreed with it yet, or "accepted" once it is agreed. If a later ADR changes or reverses a decision, it may be marked as "deprecated" or "superseded" with a reference to its replacement.

## Context 

This section describes the forces at play, including technological, political, social, and project local. These forces are probably in tension, and should be called out as such. The language in this section is value-neutral. It is simply describing facts.

## Decision

This section describes our response to these forces. It is stated in full sentences, with active voice. "We will ..."

## Consequences

This section describes the resulting context, after applying the decision. All consequences should be listed here, not just the "positive" ones. A particular decision may have positive, negative, and neutral consequences, but all of them affect the team and project in the future.
```

## Consequences

* We have to make an effort to write an ADR each time an important architectural decision is made
* We will have a complete history of all architectural decisions records 


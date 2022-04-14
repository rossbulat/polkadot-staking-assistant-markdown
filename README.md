# Polkadot Staking Assistant Markdown

> This project is a work in progress, and should only be used for testing and development purposes.

This repository hosts Markdown documents for the Polkadot Staking Dashboard Assistant. Markdown files make it easy to both configure and browse content for the assistant.

## Special Keys

We use a double-colon convention to separate each section of the document. Double-colons are not interpreted by Markdown and will appear unformatted if viewed within a Markdown document.

The Assistant transformer relies on these keys to understand how to interpret the content provided:

```
::key           <- always line 1, identifier for the document. Replace `key` with a unique value
::definitions   <- hosts definitions
::external      <- hosts external links
```

## Definitions

A definition is defined by using a H1 as its title, followed by any conventional markdown for its description. A subsequent H1 will signal the start of a new definition.

#### Example
```
# Epoch

An epoch is another name for a session in Polkadot. A different set of validators are selected to validate blocks at the beginning of every epoch.

1 epoch is currently 4 hours in Polkadot.
```

## External Links

An external link is defined by using a H1 as its title, followed by an optional subtitle, and a URL. A subsequent H1 will signal the start of a new external.

When formatting an external:
- Subtitles can be omitted.
- The URL link text acts as a label within the Assistant UI. 

#### Example
```
# Understanding Payouts

[Tutorials](https://polkadot.network/)
```

## Example Document

The following document is a clipped version of `Validators.md`, demonstrating the usage of all content types:

```
::validators
::definitions

# Minimum Nomination Bond

The minimum amount you need bonded in order to nominate.

# Commission

Validators can take a percentage of the rewards they earn. This chunk is called their commission.

Nominating validators with low commissions mean you will receive a larger share of the rewards they generate.

Many validators will have a commission rate of 100%, meaning you will receive no rewards by nominating these validators.

Examples of such validators include those operating on behalf of exchanges, where nominating and reward distribution is done centrally on the exchange in question.

A validator can update their commission rates as and when they please, and such changes will have an impact on your profitability. Be sure to monitor your nominations on this dashboard to keep updated on their commission rates.

::external

# Choosing Validators: What to Know?

[Tutorials](https://polkadot.network/)
```
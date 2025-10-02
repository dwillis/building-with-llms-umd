# Building software on top of Large Language Models for CMSC398z

For presentation in UMD's [CMSC 398z](https://www.cs.umd.edu/class/fall2025/cmsc398z/) Oct 3rd, 2025, which is offered by [Bill Pugh](https://www.cs.umd.edu/~pugh) and [Derek Willis](https://merrill.umd.edu/directory/derek-willis).

These slides have been adapted from a workshop presented by [Simon Willison](https://simonwillison.net) at PyCon 2025.

See [Simon's blog for his accompanying annotated slides](https://simonwillison.net/2025/May/15/building-on-llms/) and
the [original github repository](https://github.com/simonw/building-with-llms-pycon-2025).

As a resource, you might want to also look at [Full documentation of llm](https://llm.datasette.io/en/stable/index.html).

Among other changes, we

* Updated the model used from gpt-4.1-mini to gpt-5-mini,
* Use uv for managing python dependencies rather than pip,
* So far, only cover about half of the material in Simon's workshop,
* Have more discussion of correct and consistent data extraction
* Describe projects for week 5 of CMSC 398z
* Replaced all references to pelicans with terrapins.

We plan to cover much of the rest of the material in Simon's workshop on Oct 10th.

```{toctree}
---
maxdepth: 3
---
setup
prompting
structured-data-extraction
prompting-python
correct-extraction
week5-project
```

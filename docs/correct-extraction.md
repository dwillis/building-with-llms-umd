# Correct and consistent extraction

You are well aware that LLM's do not generate text consistently. If you ask it for ten jokes about a terrapin, it will likely give you different answers each time. Many models have a way that you can specify the seed used for its random number generation, so that it will return consistent results.

For example, if you use

```bash
 llm -o seed 0  "give me 5 funny names for a terrapin"
```

you should get the same 5 names each time you run it. Some models have other ways of modifying how output tokens are selected (such as changing the temperature), but some recent models, such as gpt-5, don't provide these.

But when we are trying to extract data from fragment, attachment or text, we ideally want to do so correctly. A particular problem is that when models are asked to extract data, they are generally reluctant to say "I don't know".

When using a LLM for data extraction, we want to have a feeling as to how accurate we expect this extraction to be, and ideally, label data that is unknown, known with low confidence, or inconsistent.
We have several approaches we can take here:

* Run the extraction multiple times, and compare the results.
  * If the results are not textually identical, try to determine if they are semantically equivalent
  * If we have ground truth for some examples, compare results to ground truth.
* Run the extraction multiple times, and use an answer only if a high percentage of attempts give the equivalent answers.
* If the data being extracted contains redundant information, you can check that to see if the data is consistent. Perhaps there is a total column which should be equal to the sum of other columns.
* Ask the model to provide a NA result for a field if it cannot confidently extract a value, or provide a confidence value for a record. I've not had good luck with getting this to work, but maybe you can.




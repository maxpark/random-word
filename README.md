# random-word

This is a simple python package to generate random english words.
If you need help after reading the below, please find me at @vaibhavsingh97 on Twitter.

## Basic Setup

You should be able to install using `easy_install` or `pip` in the usual ways:

```sh
$ easy_install random-word
$ pip install random-word
```

Or just clone this repository and run:

```sh
$ python3 setup.py install
```

Or place the `random-word` folder that you downloaded somewhere where it can be accessed by your scripts.

## Basic Usage

```python
from random_word import RandomWords
r = RandomWords()

# Return a single random word
r.get_random_word()
# Return list of Random words
r.get_random_words()
# Return Word of the day
r.word_of_the_day()
```

## Advance Usage

1. To generate single random word we can ue these optional parameters

    - hasDictionaryDef (string) -  Only return words with dictionary definitions (optional)
    - includePartOfSpeech (string) -  CSV part-of-speech values to include (optional)
    - excludePartOfSpeech (string) -  CSV part-of-speech values to exclude (optional)
    - minCorpusCount (integer) -  Minimum corpus frequency for terms (optional)
    - maxCorpusCount (integer) -  Maximum corpus frequency for terms (optional)
    - minDictionaryCount (integer) -  Minimum dictionary count (optional)
    - maxDictionaryCount (integer) -  Maximum dictionary count (optional)
    - minLength (integer) -  Minimum word length (optional)
    - maxLength (integer) -  Maximum word length (optional)

    ```python
    r.get_random_word(hasDictionaryDef="true", includePartOfSpeech="noun,verb", minCorpusCount=1, maxCorpusCount=10, minDictionaryCount=1, maxDictionaryCount=10, minLength=5, minLength=10)

    # Output: pediophobia
    ```

2. To generate list of random word we can ue these optional parameters

    - hasDictionaryDef (string) -  Only return words with dictionary definitions (optional)
    - includePartOfSpeech (string) -  CSV part-of-speech values to include (optional)
    - excludePartOfSpeech (string) -  CSV part-of-speech values to exclude (optional)
    - minCorpusCount (integer) -  Minimum corpus frequency for terms (optional)
    - maxCorpusCount (integer) -  Maximum corpus frequency for terms (optional)
    - minDictionaryCount (integer) -  Minimum dictionary count (optional)
    - maxDictionaryCount (integer) -  Maximum dictionary count (optional)
    - minLength (integer) -  Minimum word length (optional)
    - maxLength (integer) -  Maximum word length (optional)
    - sortBy (string) -  Attribute to sort by `alpha` or `count` (optional)
    - sortOrder (string) -  Sort direction by `asc` or `desc` (optional)
    - limit (integer) -  Maximum number of results to return (optional)

    ```python
    r.get_random_words(hasDictionaryDef="true", includePartOfSpeech="noun,verb", minCorpusCount=1, maxCorpusCount=10, minDictionaryCount=1, maxDictionaryCount=10, minLength=5, maxLength=10, sortBy="alpha", sortOrder="asc", limit=15)

    # Output: ['ambivert', 'calcspar', 'deaness', 'entrete', 'gades', 'monkeydom', 'outclimbed', 'outdared', 'pistoleers', 'redbugs', 'snake-line', 'subrules', 'subtrends', 'torenia', 'unhides']
    ```

3. To get word of the day

    - date (string) -  Fetches by date in yyyy-MM-dd (optional)

    ```python
    r.word_of_the_day(date="2018-01-01")

    # Output: {"word": "qualtagh", "definations": [{"text": "The first person one encounters, either after leaving one\'s home or (sometimes) outside one\'s home, especially on New Year\'s Day.", "source": "wiktionary", "partOfSpeech": "noun"}, {"text": "A Christmas or New Year\'s ceremony, in the Isle of Man; one who takes part in the ceremony. See the first extract.", "source": "century", "partOfSpeech": "noun"}]}
    ```

## Issues

You can report the bugs at the [issue tracker](https://github.com/vaibhavsingh97/random-word/issues)

## License

Built with ♥ by Vaibhav Singh([@vaibhavsingh97](https://github.com/vaibhavsingh97)) under [MIT License](https://vaibhavsingh97.mit-license.org/)

You can find a copy of the License at <https://vaibhavsingh97.mit-license.org/>

# UzbekStemmer
A Uzbek language stemmer for Python

All studies on uzbek language stemmers have a common statement: stemming of Uzbek language is hard. Uzbek is an agglutinative language with a highly rich morphological structure. Uzbek words are composed of a stem and of affix(es). In Uzbek language, there is two form of affixes: prefixes and suffixes. Affixes are affixed to the stem according to definite grammatical rules. In addition, both stem and affixes may be transformed according to the harmony rules. Those rules and their exceptions make stemming harder for Uzbek texts. For more about stemming Uzbek language please see the article titled "UZBEK AFFIX FINITE STATE MACHINE FOR STEMMING."

All text analysis studies require a stemmer at one point. This Python code attempts to stem Uzbek words with a simple approach. It first extracts syllables of the given word and then tries to identify the stem by comparing syllables with a list of affixes and their allomorphs. If any affix is identified it is removed and then remaining word is searched in a list of Uzbek words. If there is a match in the word list, it is returned as the stem. Otherwise function reiterates with the new word. If it can't stem, it returns the given word.

Once the functions are loaded into Python environment you can begin to stem by using <code>stem</code> function: <pre>stem("maktablarimizning")</pre>

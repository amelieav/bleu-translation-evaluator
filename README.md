# Translation Quality Evaluation Script

This Python script is designed for evaluating the quality of translations generated by a chatbot using the BLEU (Bilingual Evaluation Understudy) metric.

### How to Use

Ensure you have the necessary dependencies installed. You can install them using nltk:

`pip install nltk`

Create a list of reference texts and a corresponding list of generated texts for evaluation.

#### Use the provided functions as follows:

`evaluate_chatbot_responses(references, generated_texts):` Calculates BLEU scores for the reference and generated texts.

`overall_evaluation(bleu_scores, threshold=0.5):` Provides an overall evaluation based on the average BLEU score.

Customize the evaluation threshold to suit your specific use case.

## Example usage

#### French text:

La bergeronnette blanche (Motacilla alba) est un petit oiseau que l’on trouve en Europe, en Asie, en Afrique du Nord et parfois en Alaska. En Irlande et en Grande-Bretagne, une sous-espèce plus foncée appelée la bergeronnette pied (M. a. yarrellii) est commune. Il existe plusieurs sous-espèces au total.

#### A human translation

references = [
"The white wagtail (Motacilla alba) is a small bird found in Europe, Asia, North Africa, and occasionally Alaska. In Ireland and Great Britain, a darker subspecies called the pied wagtail (M. a. yarrellii) is common. There are several subspecies in total.",
]

#### Translation by a chatbot

generated_texts = [
"The white wagtail (Motacilla alba) is a small bird found in Europe, Asia, North Africa, and sometimes in Alaska. In Ireland and Great Britain, a darker subspecies called the pied wagtail (M. a. yarrellii) is common. There are several subspecies in total.",
]

### Output

`Generated BLEU Scores: [0.9312457603037672]
Overall Evaluation: Excellent`

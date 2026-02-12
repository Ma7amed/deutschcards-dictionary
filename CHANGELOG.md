Commands:

python3 build_db.py --jsonl kaikki.org-dictionary-German-words.jsonl --db deutschcards_full_v1.2.db --a1 a1_wordlist.txt --a2 a2_wordlist.txt

python3 make_core_db.py --full deutschcards_full_v1.2.db --out deutschcards_core.db

# v1.2

## Gemüse .. no plural

select * from german_words where lemma = 'Gemüse'

update german_words set plural = NULL where lemma = 'Gemüse'

# v1.3

## das Tee > der Tee

select * from german_words where lemma = 'Tee'

update german_words set  article= 'der' where lemma = 'Tee'
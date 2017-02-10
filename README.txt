Pseudocode:

# of unique species of dog: 82
cut -d ',' -f10 dog_data.csv | tail -n+16 | sort | uniq | wc -l

Counting how many unique names there are:
cut -d ',' -f10 dog_data.csv | tail -n+16 | sort | uniq -c

Matching/counting how many times the unique species occur:
cut -d ',' -f 7,10 dog_data.csv | tail -n+16 | sort | uniq -c

Extracting early intervals:
cut -d ',' -f13 dog_data.csv | tail -n+16 | sort | uniq | wc -l

Matching dog species occurrences:
	order = occurrence, name of unique species, early period
cut -d ',' -f 7,10,13 dog_data.csv | tail -n+16 | sort | uniq -c

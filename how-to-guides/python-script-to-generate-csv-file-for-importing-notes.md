# Python script to generate CSV file for importing notes

```python
import csv

# This is fixed like the CSV template
fieldnames = ['title', 'image', 'content', 'type', 'op1', 'op2', 'op3', 'op4', 'op5', 'correct_op', 'explain']

# Sample data, you can replace it with any iterator 
data = [
    ["In the Scoville scale, what is the hottest chemical?", "Resiniferatoxin"],
    ["Dry ice is the solid form of what substance?", "Carbon dioxide"],
]

with open('notes.csv', 'w', newline='') as csvfile:
    writer = csv.DictWriter(csvfile, fieldnames=fieldnames)
    writer.writeheader()

    for row in data:
        # Row data will depends on the note type
        writer.writerow({
            'title': row[0],
            'type': "Flash card", # "Multiple choice", "Type answer" or "Flash card"
            'explain': row[2],
        })

```


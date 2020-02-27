{:.py-4 .mt-4 #subjects}
***

## Subjects Page

{% include bootstrap/image.md img="/theme/subjects.jpg" %}

{% capture subject-text %}
- **subjects-fields**: Choose metadata fields from your collection metadata CSV to be included in the Subjects page tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- When this field is left blank, subjects will not be generated and the tag cloud on the Subjects page will be blank. 
	- ***Important note:*** You must also remove the "Subjects" line from the [_data/config-nav.csv](customize#config-nav) in order to remove the Subjects page from the site completely.
	- example --> `subject;creator`

- **subjects-min**: Minimum number of times a subject term must appear before being displayed in the tag cloud. 
	- Use this to improve load and build times. Too many terms = slow load time!
	- Range: `1` - `30` (note that a really large number will likely make no subjects appear)
	- example --> `subject-min: 4`

- **subjects-stopwords**: A set of words/phrases to be removed from the tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `stopwords: boxers;boxing;boxer`
{% endcapture %}

{% include bootstrap/card.md text=subject-text %}
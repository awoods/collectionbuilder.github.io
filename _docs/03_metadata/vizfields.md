---
title: Fields Required for Visualizations
stub: vis
section: metadata
section_order: 3
---

{:.py-4 .mt-4 #vis}
***

## 3. Fields Required for Visualizations
CollectionBuilder uses these fields to generate contextual visualizations, including a map, timeline, and word clouds reflecting the frequency of subjects and locations in a collection.

<table class='table table-striped float-right col-md-5 ml-2 p-0'><tr><th>Page</th><th>Required Fields</th></tr><tr><td>Map</td><td class="font-italic">latitude & longitude</td></tr><tr><td>Timeline</td><td class="font-italic">date (yyyy at min.)</td></tr><tr><td>Subjects</td><td class="font-italic">subject</td></tr><tr><td>Location</td><td class="font-italic">location</td></tr></table>


- **latitude**:
    - A geographic coordinate specifying the north-south position of an item. See the [Map](theme.html#map-page) section for more information.
    - Example Input: `46.731643`
- **longitude**:
    - A geographic coordinate specifying the east-west position of an item. See the [Map](theme.html#map-page) section for more information.
    - Example Input: `-117.165625`
- **date**: 
    - This field indicates a point in time or period of time associated with the item. 
    - Dates should be represented in the format `yyyy-mm-dd`, which will enable our various timeline visualizations. See the [Timeline](theme.html#timeline-page) section for more details. 
    - For less exact dates, `yyyy-mm` or `yyyy` may be used.
    - Example Input: `1997-07-16`, `1997-07`, `1997`
    - (Dates in a `mm/dd/yyyy` will also work)
- **subject**:
    - The subject field contains topic(s) related to the item. 
    - This field allows for multiple subjects to be input for a single record. Each should be separated with a semi-colon (`;`). 
    - See the [Subjects](theme.html#subjects-page) section for more information.
    - Example Input: `Dogs; Cats; Zebras`
{%include bootstrap/alert.md color="warning ml-4 font-small" text="*Note: This field needs to be named ***'subject' (not 'subjects'***) for many features in CollectionBuilder to work.* Data in this field will create the word cloud that allows users to visualize the amount of subjects used within the collection."%}
- **location**: 
    - This field designates a geographic location(s) to which the item is tied. Much like the subject field, this field will build a tag cloud of the most used locations in your collection. See the [Locations](theme.html#locations-page) section for more information. Be sure to separate multiple location entries for a single record with a semi-colon (`;`).
    - Example Input: `Pullman, Washington; Moscow, Idaho`

{%include bootstrap/alert.md color="success ml-4 font-small" text="*Note*: **If your metadata does not have map coordinates**, but you would like to experience CollectionBuilder's map visualization, we've created a [demo list of latitudes and longitudes](https://docs.google.com/spreadsheets/d/1eSj7zfthuc7-ntdnZLqNYETxVa5Z55YK8BPPao53-6w/edit?usp=sharing) that you can add to your data just for practice."%}
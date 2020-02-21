 Refer to the [.theme.yml section](theme.html) for more information about customizing the various pages in your collection. 

The files discussed in this section will help you customize the website to fit the metadata that's driving it. Each of these files is a CSV (comma separated values) file that is stored in the /_data/ directory of your repository. You can edit this using your text editor (recommended) or you can edit them using excel, Google Sheets, or another spreadsheet program. 

- [Navigation Header Configuration](#config-nav) (config-nav.csv)
    - configure the navigation links in the header
- [Metadata / Item Page Configuration](#config-metadata) (config-metadata.csv)
    - configure how metadata appears on item pages
- [Browse Page Configuration](#config-browse) (config-browse.csv)
    - configure the information on the browse cards for items
- [Map Page Configuration](#config-map) (config-map.csv)
    - configure what appears in the map pop-ups
- [Table Configuration](#config-table) (config-table.csv)
    - configure what metadata appears in the table visualization

{:.py-4 .mt-4 #config-nav}
***

## Navigation Header Configuration (config-nav.csv)

This CSV controls what and in what order the links appear in your header's navigation bar. 

- **display_text**: This field determines what words will display in the nav bar. 
- **stub**: This field determines what link the display text will follow. 
- **dropdown_parent**: This field is used to add dropdown functionality to your nav bar. Use it to indicate items that should appear inside a dropdown menu. It should be left empty for any non-dropdown nav item. Follow these rules to configure your nav dropdown:
    - If the item has a `stub`, but no value in `dropdown_parent`, it becomes a normal nav item
    - If the item has no `stub`, it will become a dropdown menu
    - If the item has a value in `dropdown_parent`, it will only show up under the parent dropdown

### Example

{:.pl-4}
```
    display_text,stub,dropdown_parent
    Home,/,
    Browse,/browse.html,
    Subjects,/subjects.html,
    Map,/map.html,
    Timeline,/timeline.html,
    Data,/data/,
    About,,
    About the Collection,/about.html,About
    CollectionBuilder,/tech.html,About
```

The above CSV will create 7 links in the nav bar for the referenced pages. These same nav items will also automatically appear in the footer. The last two lines of this CSV will appear within the "About" dropdown menu. "About" (because it has no value in `stub` or `dropdown_parent`) will appear in the nav bar as a dropdown button. When clicked, the dropdown menu will appear with "About the Collection" and "CollectionBuilder" listed, both linking to their respective pages.

You might have noticed that the Locations Page has been deleted, so it won't show up in your nav bar. If you want to add it back in, you'll just need to add a line after the `Subjects,/subjects.html,` line that reads: `Locations,/locations.html,`

Note: Dropdowns do NOT appear in the footer nav. The parent will appear, with a link to the top child. 

{:.py-4 .mt-4 #config-metadata}
***

## Metadata / Item Page Configuration (config-metadata.csv)

The most important CSV (if you're measuring by the number of pages it creates!) is the one that controls the metadata. [***config-metadata.csv***](#config-metadata) controls how an item's metadata is displayed on its web page. The file provides a number of options to help control the display of the item, as well as the machine-readability/SEO indexing characteristics of the code underneath the display. The fields are described below: 

- **field**: This variable corresponds to the field listed in the metadata for the collection. For instance, if you have a metadata field called "original-collection", you would put "original-collection" here. 
- **display-name**: This variable is how you'd like the field to be described on the item page. So, using the example above, if you'd like the field "original-collection" to appear as "Original Archival Collection" on the item page, you'd enter "Original Archival Collection" in the second column.
- **browse-link**: 
    - *Options*: `true` or leave blank. 
    - You can either enter `true` in this column, or leave it blank. This option controls whether this element will be represented as a link from the item page back to the browse page. It is most useful for those fields, like "subject," that often have multiple entries. So, for instance, if you wanted to make the subjects in your "subject" field separate out into individual links, you'd enter `true` in the fourth column of the `config-metadata.csv`  
- **dc-map**: 
    - *Options*: [DC Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/), written like `DC.the_term_you_choose_from_the_site_linked`
    - If you'd like to map this piece of metadata so that it will be machine readable in the code for the page, you can enter the Dublin Core metadata field you'd like it to be represented as here. So, continuing with our original example, if you'd lke to map the "original-collection" field to be read as a Dublin Core Source element, you'd enter "DC.source" in the third column.
- **schema-map**:
    - Schema is a standard designed to provide structured semantic markup for search engines to better understand content of web pages. Item pages have in depth Schema markup in JSON-LD format driven by the object metadata. 
    - See the [Full Schema hierarchy](https://schema.org/docs/full.html) for more detail and options. Each item page is given the basic type of `CreativeWork`, thus metadata fields can be mapped to any of the properties listed on the [CreativeWork documentation](https://schema.org/CreativeWork). Copy the exact property name, as this value will be turned into schema JSON-LD markup. 
    - *Options*: Suggested field mappings include:
        - `headline` (i.e. the title)
        - `creator`
        - `dateCreated`
        - `description`
        - `keywords`
        - `contentLocation`
        - `encodingFormat` (This corresponds to the [format](metadata#required) field of CollectionBuilder items)
        - `license` (Should only be used with a standardized rights URL)

### Example 

{:.pl-4}
    field,display-name,browse-link,dc-map,schema-map
    title,Title,,DC.title,headline
    creator,Creator,,DC.creator,creator
    date,Date Created,,DCTERMS.created,dateCreated
    date-is-approximate,Approximated Date
    description,Description,,DC.description,description
    subject,Subjects,true,DC.subject,keywords
    location,Location,true,,contentLocation
    identifier,Source Identifier
    type,Type,,DC.type
    format,Format,,,encodingFormat
    rightsstatement,,,DC.rights,license

- In the case of this example:
    - Only the location and subject fields have a value (`true`) for "browse-link", which creates filter links (e.g. browse.html#dogs) back to the browse page for each location and subject delimited by semi-colon in that field. 
    - The title, creator, date, description, subject, and type fields would all be represented in an item page's "head" meta section related to the Dublin Core schema to enable better machine readability and indexing.
    - The title, creator, date, description, subject, location, format, and rightstatement fields would all be represented in an item page's "head" meta section related to Schema.org to enable better machine readability and indexing.    
 
{:.py-4 .mt-4 #config-browse}
***

## Browse Page Configuration (config-browse.csv)

The Browse page displays all the items in the collection as a "card," which is a design feature common to Bootstrap. At the top of the page, a search box allows users to limit the display by searching for certain terms. We also use subject links throughout the site that link back into the browse page and filter the collection based on the filter choosen. 

So, for instance, if on the Subjects page, you clicked a button for "Forests," you would actually be clicking a link whose url ended as "browse.html#forests." The Browse page would take anything after the hashtag ('#') and filter the collection's cards by it. 

The Browse page configuration CSV allows you to control which metadata appears on a card for each item. Title and date (if it's there) appear automatically. After that, you can add whatever metadata you'd like, as well as determine how that metadata will be displayed. 

- **field** - determines the field that is displayed
- **display-name** - 
- **btn** - Determines whether that metadata displays as a button or if it should be prefaced by a label. 
    - *Options*: either "btn" or any other text you'd like to use as a label for the field. 
    - "btn" will all metadata in that field into buttons, and is recommend for fields that have mutiple entries, like 'subject.' 
- **hidden** - 

To turn the metadata in a field, such as the 'subject' field, into buttons that encourage the user to click them and filter the collection by that term, you simply need to define the field in the first column and then write "btn" in the second column. So, for a subject field, that would look like: "subject,btn" . 

If you wanted to add, for instance, a description, and call that a description, you would write "description,Description" and if you wanted to include the description but you thought labelling it was unnecessary, you could write "description," and thereby leaving the display name blank. 



{:.py-4 .mt-4 #config-map}
***

## Map Page Configuration (config-map.csv)

The config-map.csv determines what information displays on the pop-ups on the map. More on the search option can be found on the [theme page](theme.html#map-page)

- **field** - Determines the field that is displayed on the pop-up. 
- **display** - Determines the label given to the field. 
- **search** - Determines whether the field is searchable. 
    - *Options*: 'true' or leave blank

{:.py-4 .mt-4 #config-table}
***

## Table Configuration (config-table.csv)

The table appears on the "Data" page. It uses [DataTables](https://datatables.net/) to generate a table that can be searched, sorted, and downloaded as a whole or in a filtered version.

We recommend not using more than 5 or 6 fields here, as the table can become overcrowded. 

- **field** - Determines the field that is displayed on the pop-up. 
- **display** - Determines the label given to the field. 
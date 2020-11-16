Modifications to the original data include:

Removal of the 'imported_tag_type=s' attributes from the sentence level. This attribute is just a relic from the Project Wizard and not required.
Accordingly, the respective attribute has been removed from the sentence_scheme.xml.

The np_type attribute on the coref level has been changed to a branching attribute, by adding next="level_corefclass" to all values except 'none'. This way, the coref_class attribute is only available for non-none values of np_form.
Note that this modification causes a couple of coref markables to raise validation exceptions. 

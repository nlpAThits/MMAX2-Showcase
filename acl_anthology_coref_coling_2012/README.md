Modifications to the original data include:

Removal of the 'imported_tag_type=s' attributes from the sentence level. This attribute is just a relic from the Project Wizard and not required.
Accordingly, the respective attribute has been removed from the sentence_scheme.xml.

The np_type attribute on the coref level has been changed to a branching attribute, by adding next="level_corefclass" to all values except 'none'. This way, the coref_class attribute is only available for non-none values of np_form.
Note that this modification causes a couple of coref markables to raise validation exceptions. 

A single global_common_paths.xml was added and stored in a new folder named common. This folder also contains all commonly used files, like schemes and customizations. The global_common_paths.xml file has the attribute "at_startup=visible" added to the sentence level entry. This way, the sentence level markables will be visible, but will not react to mouse clicks, significantly simplifying the annotation without having to apply this setting every time the dataset is loaded in the MMAX2 gui.

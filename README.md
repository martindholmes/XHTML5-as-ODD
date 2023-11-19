# XHTML5-as-ODD
## Building a simple XHTML5 schema from a TEI ODD file

The VNU validator (https://github.com/validator/validator/) is a wonderful tool, but it does not serve regular project purposes well. Generally speaking, for projects whose data source format is XHTML5, what is needed is a much smaller, tighter schema which can be used to enforce not only general XHTML5 validity but also project-specific rules. HTML5 is a large and growing standard, and most projects will only use a fraction of the elements and attributes available. The VNU validator contains RNC schema files for XHTML5, but those files are dependent on a datatype library which is distributed only in the form of large Java files with a lot of other content. 

So while using the VNU validator as a final check of a website produced from a build process is essential, for encoders working on content in XHTML5, a much more specific schema is very helpful, and in several projects created at HCMC[^1] I have already created such schemas. To do this I used the TEI ODD specification[^2]. The ODD specification is intended primarily for producing customizations of the TEI schema, but it can be used to create any other kind of XML schema and documentation. See my article in the *Journal of the TEI*[^3] for more information on how odd can be used for HTML.

The purpose of this project, then, is to slowly and steadily build a general-purpose XHTML5 schema which includes all of the components (elements, attributes, and constraints) required by projects using XHTML5 as a data format, to provide a clean and simple starting point for future projects. As this schema grows, projects will probably need to apply customizations to it, removing things they don't need, and possibily adding their own customizations such as Schematron rules specific to their project. This can be done with TEI ODD chaining.


[^1]: Examples: [Then & Now](https://eb11.uvic.ca/), [The HCMC Journal](https://hcmc.uvic.ca/journal/public/), [Mapping Keats’s Progress: A Critical Chronology
Mapping Keats’s Progress](https://johnkeats.uvic.ca).
[^2]: https://tei-c.org/guidelines/customization/getting-started-with-p5-odds/
[^3]: Martin Holmes. 2021. "Using ODD for HTML." *The Journal of the Text Encoding Initiative*. Text Encoding Initiative Consortium. 2021. [https://journals.openedition.org/jtei/3106]. 
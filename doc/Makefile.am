## Process this file with automake to produce Makefile.in
## Copyright: Sámediggi/Divvun/UiT
## Licence: GPL v3+

# List all jspwiki files that should be created from source files in the
# JSP_PAGES variable. The filename pattern is as follows:
#
# dir/filename.lexc => filename-dir.jspwiki

if CAN_DOCC

JSP_PAGES=root-morphology.jspwiki        \
		  adjectives-affixes.jspwiki       \
		  nouns-affixes.jspwiki          \
		  possessive-suffixes-affixes.jspwiki \
		  verbs-affixes.jspwiki \
		  abbreviations-stems.jspwiki      \
		  acronyms-stems.jspwiki           \
		  adjectives-stems.jspwiki         \
		  adpositions-stems.jspwiki        \
		  adverbs-stems.jspwiki            \
		  conjunctions-stems.jspwiki       \
		  nouns-stems.jspwiki              \
		  numerals-stems.jspwiki           \
		  particles-stems.jspwiki          \
		  pronouns-stems.jspwiki           \
		  sme-propernouns-stems.jspwiki        \
		  subjunctions-stems.jspwiki       \
		  verbs-stems.jspwiki              \
		  disambiguation-syntax.jspwiki \
		  functions-syntax.jspwiki \
		  dependency-syntax.jspwiki  
# clitics-morphology.jspwiki       \
# compounding-morphology.jspwiki   \
# adjectives-oahpa-stems.jspwiki   \
# interjections-stems.jspwiki      \
# nouns-oahpa-stems.jspwiki        \
# punctuation-stems.jspwiki        \
# smi-propernouns-stems.jspwiki    \
# adjectives-oahpa-affixes.jspwiki \
# propernouns-affixes.jspwiki      \
ALLINONE_JSP_PAGE=$(srcdir)/$(GTLANG).jspwiki

LINKS=$(srcdir)/Links.jspwiki

endif # CAN_DOCC

include $(top_srcdir)/am-shared/doc-dir-include.am

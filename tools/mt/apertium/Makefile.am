## Process this file with automake to produce Makefile.in
## Copyright: Sámediggi/Divvun/UiT
## Licence: GPL v3+

# Process subdirs first:
SUBDIRS = filters tagsets .

##################################################################
#### Specify target languages and corresponding file names:   ####
##################################################################

# Specify the list of target languages and their corresponding
# Apertium directory names in these two variables (replace und):
APERTIUM_TARGET_LANGS=sma smj smn nob fin
APERTIUM_TARGET_LANG_NAME=apertium-sme-sma \
						  apertium-sme-smj \
						  apertium-sme-smn \
						  apertium-sme-nob \
						  apertium-sme-fin

##################################################################
#### BEGIN: Add local processing instructions BELOW this line ####
##################################################################

# We want to make semantic tags optional for the apertium-targeted analyser:
analyser-mt-gt-desc.%.hfst: analyser-mt-gt-desc.%.tmp.hfst \
			$(top_builddir)/src/filters/make-optional-semantic-tags.hfst
	$(AM_V_RGX2FST)$(PRINTF) "\
		@\"$(top_builddir)/src/filters/make-optional-semantic-tags.hfst\" \
   	.o. @\"$<\" \
    	;" \
		| $(HFST_REGEXP2FST) $(HFST_FLAGS) -S --xerox-composition=ON \
		| $(HFST_INVERT) $(HFSTFLAGS) \
		| $(HFST_FST2FST) $(HFSTFLAGS) -t \
		-o $@

##################################################################
#### END: Add local processing instructions ABOVE this line ######
##################################################################

####### Other targets: ###########

# cleaning
clean-local:
	-rm -f *.hfst *.gz *.cg3 *.bin *.hfstol

include $(top_srcdir)/am-shared/tools-mt-apertium-dir-include.am

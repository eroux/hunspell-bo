DEBIAN_FILES = changelog copyright rules watch compat hunspell-bo.info-hunspell hunspell-bo.links source control hunspell-bo.install

ORIG_FILES = ../bo.dic ../bo.aff ../CHANGELOG.md

VERSION = 0.4.0

all: deb

orig: $(DEBIAN_FILES) $(ORIG_FILES)
	@echo "Making orig.tar.gz archive..."
	@mkdir -p hunspell-bo && cp $(ORIG_FILES) hunspell-bo
	@tar czf hunspell-bo_$(VERSION).orig.tar.gz hunspell-bo

deb: orig
	@echo "Making .deb package..."
	@mkdir -p hunspell-bo/debian
	@cp -R $(DEBIAN_FILES) hunspell-bo/debian
	@cd hunspell-bo && dpkg-buildpackage

clean:
	@rm -rf *.deb *.xz *.gz *.dsc *.changes *.upload

all: oxt

# https://wiki.openoffice.org/wiki/Documentation/DevGuide/Extensions/File_Format

FILES=dictionaries.xcu description.xml package-description.txt

oxt: $(FILES) ../README.md ../CHANGELOG.md ../bo.dic ../bo.aff META-INF/manifest.xml
	@echo "Making oxt file for LibreOffice..."
	@cp ../bo.dic ../bo.aff .
	@cp ../README.md .
	@zip -rq tibetan-spellchecker.oxt bo.dic bo.aff $(FILES) META-INF README.md CHANGELOG.md

clean:
	@rm -f bo.dic bo.aff README.md CHANGELOG.md tibetan-spellchecker.oxt

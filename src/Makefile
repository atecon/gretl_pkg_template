PKG = kmeans

$(PKG).gfn: $(PKG).inp $(PKG).spec $(PKG)_sample.inp
	gretlcli --makepkg $(PKG).inp

$(PKG).zip: $(PKG).gfn ./docs/$(PKG).pdf
	echo makepkg $(PKG).zip | gretlcli -b -

install: $(PKG).zip
	echo pkg install $(PKG).zip --local | gretlcli -b -

clean:
	rm -f $(PKG).zip

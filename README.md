# sedscripts

A collection of of random and useful (and not so useful) sedscript files for use with 'sed -f':


## fix_tw_centos7.3.sed

A sed script used to fix tripwire on centos7.3 with regards to error report about 147 missing files, to alleviate yourself from this myriad of errors, run the following assuming a clean install of tripwire:

	# cd /etc/tripwire
	# sed -i.bak -r -f fix_tw_centos7.3.sed twpol.txt

Then follow the standard configuration procedure as outlined in /usr/share/doc/tripwire-*/README.Fedora 

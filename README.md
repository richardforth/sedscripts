# sedscripts

A collection of of random and useful (and not so useful) sedscript files for use with 'sed -f':


## fix_tw_centos7.3.sed

A sed script used to fix tripwire on centos7.3 with regards to error report about 147 missing files, to alleviate yourself from this myriad of errors, run the following assuming a clean install of tripwire:

	# cd /etc/tripwire
	# sed -i.bak -r -f fix_tw_centos7.3.sed twpol.txt

Then follow the standard configuration procedure as outlined in /usr/share/doc/tripwire-\*/README.Fedora 

## countries.sed

A sed script that will convert any 2 digit country codes into long names, useful when doing whois type lookips on IP addresses.


## distros-tbl.sed  and distros.txt

       $ sort -k 1,1 -k 2n distros.txt | sed -f distros_tbl.sed | groff -t -T ascii 2>/dev/null | sed 'N;/^\n$/d;P;D'
                 +------------------------------+
                 |  Linux Distribution Report   |
                 +------------------------------+
                 | Name    Version    Released  |
                 +------------------------------+
                 |Fedora     5       03/20/2006 |
                 |Fedora     6       2006-10-24 |
                 |Fedora     7       2007-05-31 |
                 |Fedora     8       2007-11-08 |
                 |Fedora     9       2008-05-13 |
                 |Fedora    10       2008-11-25 |
                 |SUSE      10.1     2006-05-11 |
                 |SUSE      10.2     2006-12-07 |
                 |SUSE      10.3     2007-10-04 |
                 |SUSE      11.0     2008-06-19 |
                 |Ubuntu     6.06    2006-06-01 |
                 |Ubuntu     6.10    2006-10-26 |
                 |Ubuntu     7.04    2007-04-19 |
                 |Ubuntu     7.10    2007-10-18 |
                 |Ubuntu     8.04    2008-04-24 |
                 |Ubuntu     8.10    2008-10-30 |
                 +------------------------------+


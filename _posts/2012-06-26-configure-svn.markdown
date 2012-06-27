---
layout: default
title: Configure your Subversion-client
description: A quick guide to properly configure the subversion client
categories: advanced
---

To ensure proper line endings on files setting up the following configuration is absolutely essential on your Subversion client. The configuration files are found in:

- *~/.subversion/* on Linux / Mac OS
- *%USERPROFILE%\Application Data\Subversion\\* on Windows XP
- *%USERPROFILE\AppData\Roaming\Subversion\\* on Windows 7

Add the following to your Subversion ***config***-file:

    [miscellany]
    enable-auto-props = yes
    
    [auto-props]
    # set the line endings style for cross-platform source code text files
    *.c = svn:eol-style=native;svn:keywords=Date Author Id Revision HeadURL
    *.cpp = svn:eol-style=native;svn:keywords=Date Author Id Revision HeadURL
    *.h = svn:eol-style=native;svn:keywords=Date Author Id Revision HeadURL
    *.sh = svn:executable;svn:eol-style=native;svn:keywords=Date Revision
    Makefile = svn:eol-style=native;svn:keywords=Date Author Id Revision HeadURL
    
    # set the line endings style for Windows source code text files
    *.cmd = svn:mime-type=text/plain;svn:eol-style=CRLF
    *.bat = svn:mime-type=text/plain;svn:eol-style=CRLF
    
    # binary files
    *.obj = svn:mime-type=application/octet-stream
    *.bin = svn:mime-type=application/octet-stream
    *.bmp = svn:mime-type=image/bmp
    *.class = svn:mime-type=application/java
    *.doc = svn:mime-type=application/msword
    *.exe = svn:mime-type=application/octet-stream
    *.gif = svn:mime-type=image/gif
    *.gz = svn:mime-type=application/x-gzip
    *.jar = svn:mime-type=application/java-archive
    *.jelly = svn:mime-type=text/plain;svn:eol- style=native;svn:keywords=Date Revision
    *.jpg = svn:mime-type=image/jpeg
    *.jpeg = svn:mime-type=image/jpeg
    *.pdf = svn:mime-type=application/pdf
    *.png = svn:mime-type=image/png
    *.tgz = svn:mime-type=application/octet-stream
    *.tif = svn:mime-type=image/tiff
    *.tiff = svn:mime-type=image/tiff
    *.zip = svn:mime-type=application/zip
    
    # other text files
	*.txt = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.xml = svn:mime-type=text/xml;svn:eol-style=native;svn:keywords=Date Revision
	*.ent = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.dtd = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.vsl = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.xsd = svn:mime-type=text/xml;svn:eol-style=native;svn:keywords=Date Revision
	*.xsl = svn:mime-type=text/xml;svn:eol-style=native;svn:keywords=Date Revision
	*.wsdl = svn:mime-type=text/xml;svn:eol-style=native;svn:keywords=Date Revision
	*.htm = svn:mime-type=text/html;svn:eol-style=native;svn:keywords=Date Revision
	*.html = svn:mime-type=text/html;svn:eol-style=native;svn:keywords=Date Revision
	*.css = svn:mime-type=text/css;svn:eol-style=native;svn:keywords=Date Revision
	*.js = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.jsp = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.txt = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.java = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.properties = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date 	Revision
	*.sql = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.cmake = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.ui = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	
	# latex
	*.tex = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.bib = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.sty = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	*.aux = svn:mime-type=text/plain;svn:eol-style=native;svn:keywords=Date Revision
	
	# set all of the line endings for GeoSys model binary files
	#*.sts = svn:mime-type= binary?
	
	# set all of the line endings for GeoSys model text files
	*.mmp = svn:eol-style=native
	*.pcs = svn:eol-style=native
	*.pct = svn:eol-style=native
	*.gem = svn:eol-style=native
	*.rfd = svn:eol-style=native
	*.fct = svn:eol-style=native
	*.ddc = svn:eol-style=native
	*.rfd = svn:eol-style=native
	*.rfe = svn:eol-style=native
	*.rfi = svn:eol-style=native
	*.rfo = svn:eol-style=native
	*.msg = svn:eol-style=native
	*.sv1 = svn:eol-style=native
	*.sv2 = svn:eol-style=native
	*.rfm = svn:eol-style=native
	*.rfg = svn:eol-style=native
	*.rfv = svn:eol-style=native
	*.rfp = svn:eol-style=native
	*.pqc = svn:eol-style=native
	*.chm = svn:eol-style=native
	*.tec = svn:eol-style=native
	*.vtk = svn:eol-style=native
	*.csv = svn:eol-style=native
	*.bc = svn:eol-style=native
	*.out = svn:eol-style=native
	*.msp = svn:eol-style=native
	*.krc = svn:eol-style=native
	*.mcp = svn:eol-style=native
	*.mfp = svn:eol-style=native
	*.ic = svn:eol-style=native
	*.num = svn:eol-style=native
	*.tim = svn:eol-style=native
	*.st = svn:eol-style=native
	*.ply = svn:eol-style=native
	*.tin = svn:eol-style=native
	*.csv = svn:eol-style=native
	*.tec = svn:eol-style=native
	*.gli = svn:eol-style=native
	*.gsp = svn:eol-style=native
	*.shp = svn:eol-style=native
	*.msh = svn:eol-style=native
    ogs = svn:executable
    ogs-gui = svn:executable

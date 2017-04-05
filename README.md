## Synopsis

CliDEID is a command line tool for the de-identification of clinical narratives. It was developed as part of the CEGS N-GRID 2016 text mining challenge and therefore has been trained and optimised on the challenge data.

For example, for input:

Mr. Smith was admitted to the ABCD hospital.
He is 50 years old and works as a mechanic.
Visit with Dr. Ramirez on 10/21/2077.

CliDEID will produce the following output (stand-off):

<?xml version="1.0" encoding="UTF-8" ?>
<NGRID_deId>
<TEXT><![CDATA[Mr. Smith was admitted to the ABCD hospital.
He is 50 years old and works as a mechanic.
Visit with Dr. Ramirez on 10/21/2077 .
]]></TEXT>
<TAGS>
<AGE id="P0" start="52" end="54" text="50" TYPE="AGE" comment="" />
<DATE id="P1" start="117" end="127" text="10/21/2077" TYPE="DATE" comment="" />
<NAME id="P2" start="106" end="113" text="Ramirez" TYPE="DOCTOR" comment="" />
<LOCATION id="P3" start="30" end="34" text="ABCD" TYPE="HOSPITAL" comment="" />
<PROFESSION id="P4" start="80" end="88" text="mechanic" TYPE="PROFESSION" comment="" />
<NAME id="P5" start="4" end="9" text="Smith" TYPE="PATIENT" comment="" />
</TAGS>
</NGRID_deId>

More details on the architecture and the performance of the tool can be found in the paper below. Please cite this publication if you use CliDEID:
Dehghan A., Kovačević A., Karystianis G, Keane JA., & Nenadic, G. (2017). Learning to identify protected health information by integrating knowledge- and data-driven algorithms: a case study on psychiatric evaluation notes. Journal of Biomedical Informatics. Submitted.

Currently only binary version of CliDEID is avilable. The open source version will be made avilable in the near future.

## Installation

Please se the CliDEID_guide.pdf located in the /doc folder for installation instructions.

## License

CliDEID is copyrighted free software by Aleksandar Kovacevic <kocha78@uns.ac.rs,http://informatika.ftn.uns.ac.rs/AleksandarKovacevic/>, and is released under any of the LGPL (see the file LGPL) or the BSD License (see the file BSD).

Exclusions:

  1. For the CRF++ binaries see the copyright statement included in the crf++ directory.
  2. For cTAKES see the copyright statement included in the cTAKES directory.

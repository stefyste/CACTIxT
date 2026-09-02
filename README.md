# CACTIxT

**CACTIxT** is a CACTI-compatible framework for architectural modeling and design-space exploration of SRAM macros based on 6T, 8T, and 10T bitcell topologies.

CACTIxT extends the CACTI/FinCACTI modeling infrastructure with topology-aware models for advanced SRAM bitcells and their peripheral circuitry, including read/write wordline drivers, 
bitline discharge, sensing, pre-charge energy, leakage, area, and delay-related analyses.

## Repository contents

The repository contains:

- `CACTIxT_CodeBL/` - complete Code::Blocks project, C/C++ source files, executable files, and XML configuration files.
- `CACTIxT_CodeBL/xmls/` - memory, device/technology, and SRAM-bitcell XML configuration files.
- `source_files/` - CACTIxT C/C++ source and header files.
- `CACTIxT_User_Guide.docx` - detailed instructions for configuring and running CACTIxT.
- `CACTIxT_License.docx` - license, attribution, and citation information.
- `CACTIxT.zip` - all the above files.

The main program entry point is `main.cc`.

## Getting started

To run CACTIxT using Code::Blocks:

1. Open:

   CACTIxT_CodeBL/CACTIxT_CodeBL.cbp

2. In Code::Blocks, open **Project > Set program's arguments** and verify that the following argument is specified for the selected build target:

   -infile ./xmls/cache_config_cmos.xml

3. Configure the memory architecture, target technology, operating conditions, and SRAM bitcell topology in:

   CACTIxT_CodeBL/xmls/cache_config_cmos.xml

4. For CMOS SRAM analysis, select one of the supplied 6T, 8T, or 10T bitcell descriptions in `xmls/sram_cells/` and the appropriate technology description in `xmls/devices/`.

For detailed configuration instructions, including technology parameters and threshold-voltage variability settings, see **`CACTIxT_User_Guide.docx`**.

## Citation

If you use **CACTIxT**, or results generated using CACTIxT, in academic or scientific work, please cite **CACTIxT, CACTI, and FinCACTI**.

### CACTIxT

[AUTHORS],  
**"CACTIxT: A Unified CACTI-Compatible Framework for Architectural Exploration of Modern SRAM Bitcell Topologies,"**  
*ACM Transactions on Design Automation of Electronic Systems (TODAES)*, 2026.  
DOI: [DOI TO BE ADDED]

@article{cactixt,
  author  = {[AUTHORS]},
  title   = {{CACTIxT: A Unified CACTI-Compatible Framework for Architectural Exploration of Modern SRAM Bitcell Topologies}},
  journal = {ACM Transactions on Design Automation of Electronic Systems},
  year    = {2026},
  doi     = {[DOI]}
}

### CACTI

N. Muralimanohar, R. Balasubramonian, and N. P. Jouppi,  
**"CACTI 6.0: A Tool to Model Large Caches,"**  
HP Laboratories, Technical Report HPL-2009-85, 2009.

@techreport{cacti6,
  author      = {Muralimanohar, Naveen and Balasubramonian, Rajeev and Jouppi, Norman P.},
  title       = {{CACTI 6.0: A Tool to Model Large Caches}},
  institution = {HP Laboratories},
  number      = {HPL-2009-85},
  year        = {2009}
}

### FinCACTI

A. Shafaei, Y. Wang, X. Lin, and M. Pedram,  
**"FinCACTI: Architectural Analysis and Modeling of Caches with Deeply-Scaled FinFET Devices,"**  
*IEEE Computer Society Annual Symposium on VLSI*, 2014.

@misc{fincacti,
  author = {Shafaei, A. and Wang, Y. and Lin, X. and Pedram, M.},
  title  = {{FinCACTI: Architectural Analysis and Modeling of Caches with Deeply-Scaled FinFET Devices}},
  year   = {2014},
  note   = {IEEE Computer Society Annual Symposium on VLSI}
}

## License and attribution

CACTIxT is a CACTI-compatible extension derived in part from the **CACTI** and **FinCACTI/PCACTI** source codes.
Original copyright and license notices associated with inherited source code must be retained.

CACTIxT modifications and extensions are Copyright (c) 2026 CACTIxT Authors. All Rights Reserved.

Please refer to **`CACTIxT_License.docx`** for the complete license, redistribution conditions, attribution requirements, and disclaimer.

## Disclaimer

CACTIxT is intended for architectural modeling and design-space exploration. Results obtained using CACTIxT 
should be independently validated when used for circuit implementation, reliability assessment, or design sign-off.

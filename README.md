# Week 8 – Digital Forensics with Autopsy

## Overview

This repository contains my Week 8 Digital Forensics practical assignment completed as part of the **AstraQuantum Tech Summer of Cybersecurity 2026** program.

The practical focused on investigating a publicly available forensic disk image using **Autopsy** and documenting relevant digital artifacts and findings.

## Objectives

The main objectives of this practical were to:

* Create and configure a forensic case in Autopsy.
* Add and process a forensic disk image.
* Examine files and directories within the image.
* Check for deleted files and available user activity.
* Analyze file metadata and timestamps.
* Perform keyword-based searches.
* Identify relevant forensic artifacts.
* Interpret findings while considering forensic limitations.
* Document the investigation in a structured forensic report.

## Tool Used

**Autopsy 4.23.1**

Autopsy was used for forensic image processing, artifact examination, keyword searching, and evidence analysis.

## Evidence Source

The forensic image used for this practical was obtained from **Digital Corpora**, a publicly available source of training disk images for digital forensics.

**Dataset:** NPS Test Disk Images
**Selected Image:** `ntfs1-gen2.E01`

> The original forensic image is not included in this repository. The investigation was performed on the downloaded training image while preserving the original evidence.

## Investigation Process

### 1. Case Creation

A new Autopsy case was created with the case name:

`Week8_DigitalForensics_AQT-1372`

The case was configured for the investigation and stored separately from the evidence image.

### 2. Evidence Acquisition

The `ntfs1-gen2.E01` forensic image was added to Autopsy as the data source.

The image was processed using the available Autopsy ingest modules.

### 3. File and Deleted File Examination

The file system was examined for available files and directories.

The Deleted Files section was also reviewed. No recoverable deleted files were identified during the examination.

### 4. Recent Activity Examination

Available recent-user-activity information was reviewed. No useful recent activity data was available in the examined image.

This does not prove that no user activity ever occurred; it only reflects the artifacts available to Autopsy from this image.

### 5. Metadata Analysis

Several metadata artifacts were identified.

One notable artifact was:

`20076517123273.pdf`

Observed information included:

* Owner: `sangli`
* Creation timestamp: `2007-06-05 08:29:54 PKT`
* Modification timestamp: `2007-06-05 08:30:13 PKT`
* Source file path within the forensic image

Another artifact identified was:

`NISTSP800-88_rev1.pdf`

Observed information included:

* Owner: `PC-7`
* Creation timestamp: `2006-09-11 13:01:47 PKT`
* Modification timestamp: `2006-09-11 13:04:00 PKT`
* Description: `Report`
* Source file path within the forensic image

### 6. Keyword Search

Autopsy keyword search identified email-address-related hits.

One notable finding was:

`bullock@rti.org`

The address was identified as a keyword hit within:

`Report02-3.pdf`

The keyword preview displayed matching text from the file.

This finding demonstrates that the email address was present within the identified file. It does **not**, by itself, prove that an email was sent or received by that address.

## Key Findings

The investigation identified:

* File metadata containing ownership and timestamp information.
* PDF documents within the forensic image.
* An email address identified through keyword searching.
* No recoverable deleted files in the examined Deleted Files view.
* No useful recent-user-activity artifacts available in the examined image.

## Forensic Interpretation

The identified artifacts provide evidence of information present within the forensic disk image.

File metadata can provide useful context about documents, including timestamps, ownership information, descriptions, and file paths. However, metadata alone does not conclusively establish the identity of the person who actually used the system.

Similarly, the keyword hit for `bullock@rti.org` confirms that the address was found within `Report02-3.pdf`, but it does not independently establish that an email was sent or received.

## Limitations

The investigation has several limitations:

* The absence of deleted files does not prove that files were never deleted.
* The absence of recent activity artifacts does not prove that no user activity occurred.
* File ownership metadata does not conclusively identify the actual person using the computer.
* A keyword hit does not independently prove an email communication occurred.

## Screenshots

The `Screenshots` folder contains selected evidence from the investigation, including:

1. Autopsy case creation
2. Forensic image processing
3. Metadata artifact
4. Additional artifact details
5. Keyword search result

## Report

The complete forensic report is available in the `Report` folder.

**Report:**
`Mariam_Fatima_AQT-1372_Week8_Digital_Forensics_Report.pdf`

## Conclusion

This practical provided hands-on experience with digital forensic investigation using Autopsy. The investigation demonstrated how forensic disk images can be examined for file metadata, timestamps, keyword hits, and other available artifacts while maintaining a cautious and evidence-based interpretation of findings.

---

**Author:** Mariam Fatima
**Program:** AstraQuantum Tech – Summer of Cybersecurity 2026
**Practical:** Week 8 – Digital Forensics
**Tool:** Autopsy 4.23.1


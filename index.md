---
layout: default
title: NIH Commons DERIVA Demo
---

### DERIVA
	
[DERIVA](http://deriva.isrd.isi.edu/) is an innovative open-source scientific asset management platform designed to support collaborative, data driven scientific investigations. DERVIA can adapt to evolving and complex data models and data types. DERIVA supports continuous FAIRness by promoting self-curation, fine-grain access control, automated creation of global unique IDs for every data element, versioning, provenance, exchange of data through structured and documented data collections (BDBags).
	
DERIVA provides authentication, fine-grained authorization, secured access, and extensive logging. The authentication service allows users to authenticate with their NIH or home institutions via [Globus Auth](https://www.globus.org/tags/globus-auth), which is an OAUTH2 authentication and authorization infrastructure widely used in NIH environments. DERIVA supports Globus Groups in fine-grained access policy.
	
### Goals of the demo

**To demonstrate faceted search and browse, BDBag export, and virtual collection capabilities.**

Users should be able to:

* Search and browse data in the repository.
* Export a selected set of data.
* Create a virtual collection consisting of samples of interest.
			
### Datasets

Datasets presented in the demo include:

* [GTEx public data set](/chaise/recordset/#1/demo:Samples) (15,598 samples). This data set includes metadata such as age, sex, tissue type, autolysis score, pathology notes, sequencing details, etc.

### Use cases

#### Use case 1: Faceted search and browse samples with WGS VCF data.

1. The user is an anonymous scientist or data common participant looking for information pertaining to samples with WGS VCF data.
2. The user goes to the DERIVA web-based faceted search portal provided by team Argon. 
3. The user perform facet search by:
	1. Click on "Library Type" to expand the facet panel, then select "WGS."
	2. Click on "WGS VCFS Files" to expand the facet panel, then select "All Records With Value."
	
	The search result shows the first 25 of 591 samples. Click [here](/chaise/recordset/#1/demo:Samples/*::facets::N4IghgdgJiBcDaoDOB7ArgJwMYFM4gBkBJAIQCUBBMgTQH0AVagBQFEQAaELACxQEtcSOPBAB1AOIBlEAF0Avu2TpseBKD4QARumjCQUHAFsUHMVNoA1AMIAxSbRt8ANjiS1JFALJMiAEQBMsgogZH6ynBAoAC60EGhOTnBRGGg4cvJAA) for the results page.	
4. The user selects the individual samples in the results and navigates to it for more details by clicking the eye icon associated with the samples.

#### Use case 2: Export metadata and VCF files of samples with samples with WGS VCF data in BDBag.

1. The user is a data common participant looking for information pertaining to samples with WGS VCF data and wants to export all the VCF data relevant to the samples.
2. The user follows Use case 1 to search for samples with WGS VCF data.
3. User logs in to the portal using Globus credentials to perform the export operation.
4. The result pane on the right should show first 25 of 591 samples. Click [here](/chaise/recordset/#1/demo:Samples/*::facets::N4IghgdgJiBcDaoDOB7ArgJwMYFM4gBkBJAIQCUBBMgTQH0AVagBQFEQAaELACxQEtcSOPBAB1AOIBlEAF0Avu2TpseBKD4QARumjCQUHAFsUHMVNoA1AMIAxSbRt8ANjiS1JFALJMiAEQBMsgogZH6ynBAoAC60EGhOTnBRGGg4cvJAA) for the results page.
5. Click "Export" at the upper right corner to export the search result in the BDBag.

#### Use case 3: Create a virtual collection of samples with WGS VCF data.

1. The user is a data common participant who wants to create a virtual collection of samples with WGS VCF data that can be cited or shared with others.
2. The user creates a collection describing the title and description of the collection.
3. The user then adds samples to the collection by clicking "Add" on top of the Sample Collection table. Click [here](/chaise/record/#1/Common:Collection/RID=1-A52J) for the resulting Collection page.
4. The user can remove memberships by clicking the "Unlink" button.
5. The user who wants to cite this collection in their publications can request a DOI by setting the "Require DOI?" field to true. A DOI will be generated. Currently this process is manual. The automation process is planned for a future release.
6. The user exports the data in the Collection by clicking "Export" on the Collection detail page (Upcoming).

	    
	    
		



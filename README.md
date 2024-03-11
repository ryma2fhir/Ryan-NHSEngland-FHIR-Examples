# NHS-England-FHIR-Examples
This repository is maintained by [Interoperability Team](https://nhsd-confluence.digital.nhs.uk/pages/viewpage.action?spaceKey=IOPS&title=Interoperability+Standards). Any queries contact us via [email](interoperabilityteam@nhs.net).

This repository will be used to contain FHIR asset examples for NHS England Programme Implementation Guides [Simplifier project](https://simplifier.net/NHS-England-Programme-Implementation-Guides/~guides).

## CapabilityStatement
The CapabilityStatement is used by the validation tool to check which profile to validate against. If no Profile is stated then the base FHIR resource will be used.

## Package Creation
- Create a new branch named package-*[programme]*
- Within the branch remove any uneccessary assets
- amend the package.json (mandatory)
  - name: uk.nhsengland.r4*[programme]*
  - description: NHS England *[programme]* FHIR Implementation Guide. *[Optional: More information, such as "for validation purposes only"]*
  - version: semantic versioning, e.g. 0.0.1 
- Go to Actions and select [Create Package](https://github.com/ryma2fhir/Ryan-NHSEngland-FHIR-Examples/actions/workflows/createPackage.yml).
  - Click Run workflow
  - Choose your branch
  - Click Run workflow (green button).
- If successful, go to the [main page](https://github.com/ryma2fhir/Ryan-NHSEngland-FHIR-Examples) and choose your branch
- download the package file [filename].tar.gz and upload to your server, e.g. AWS S3

More information on package creation, along with optional attributes for package.json, see [https://hl7.org/fhir/packages.html](https://hl7.org/fhir/packages.html).

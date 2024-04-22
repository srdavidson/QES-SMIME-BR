## Proposal to add eIDAS Qualified Electronic Signatures to Section 3.2.4.1 (4) (a) of the S/MIME BR.

#### A. Proposed text

The CA MAY rely upon a Qualified Electronic Signature per Regulation (EU) 910/2014, created using a Qualified Electronic Signature Certificate issued by a Qualified Trust Service Issuing CA bearing the qualified trust service type "http://uri.etsi.org/TrstSvc/Svctype/CA/QC" and the status "http://uri.etsi.org/TrstSvc/TrustedList/Svcstatus/granted" on a EU Trusted List. The "GRANTED" status must be effective at the time of signing (if the signature is associated with a Qualified electronic time stamp) or at the time of validation (if the signature is not associated with a Qualified electronic time stamp). The Qualified Signature Certificate used for the Qualified Electronic Signature SHALL include the Qcstatement `esi4-qcStatement-6` as specified in clause 4.2.1 of ETSI EN 319 412-5 in the `id-etsi-qct-esign` QcType as specified in clause 4.2.3 of ETSI EN 319 412-5.

#### B. Background

Section 3.2.4.1 (4) (b) of the S/MIME BR lays out the criteria to be considered by the SMCWG for approval to allow validation to be performed from a certificate supporting a digital signature applied by the Applicant.
https://github.com/cabforum/smime/blob/main/SBR.md#3241-attribute-collection-of-individual-identity

_1.	Legal context: the framework SHALL be subject to regulatory provisions, which describe the requirements imposed on the Certificate issuer/trust service provider, the legal effects of the trust services, and the corresponding Certificate levels;_

The eIDAS regulation that applies to all EU Member States describing the regulatory provisions for Qualified Trust Service Providers and the legal effects of the trust services.  See https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=uriserv%3AOJ.L_.2014.257.01.0073.01.ENG 

_2.	Identity validation: the approved Certificate levels must provide a level of assurance equivalent to that of the identity validation methods described in these Requirements;_

See Article 24(1) of eIDAS.  In addition, ETSI EN 319 411-2 (https://www.etsi.org/deliver/etsi_en/319400_319499/31941102/02.05.01_60/en_31941102v020501p.pdf) describes the policy and security requirements for TSPs issuing Qualified certificates, which includes normative references to other ETSI standards on vetting including ETSI TS 119 461 (identity proofing of trust service subjects, see https://www.etsi.org/deliver/etsi_ts/119400_119499/119461/01.01.01_60/ts_119461v010101p.pdf).  

_3.	Supervision and auditing systems: the framework SHALL include appropriate rules providing for:_

_a.	supervision to ensure that trust service providers meet regulatory-imposed provisions;_

See Article 17 (Supervisory body) and Article 20 (Supervision of qualified trust service providers) of eIDAS.

_b.	requirements imposed on auditing bodies when conducting audits; and_

See Regulation (EC) No 765/2008 https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:218:0030:0047:en:PDF 

_c.	supervision of the auditing bodies._

Under Regulation (EC) No 765/2008, each Member State must develop a National Accreditation Body (NAB) that attests the competence and impartiality of a Conformity Assessment Body (CAB) according to international standards (such as ISO or ETSI).

In the context of eIDAS, a CAB is further defined as a body which is accredited as competent to carry out conformity assessment of a qualified TSP and the qualified trust services it provides. An informative list of the CABs may be found at https://eidas.ec.europa.eu/efda/browse/notification/cab-nab 

_4.	Best practices and transparency: the requirements of the trust service framework and evidence of supervision of the approved trust service providers SHALL be publicly available. The trust service framework shall require trust service providers to disclose their practices in a publicly available CP and/or CPS._

Relevant ETSI standards applying to Trust Service Providers may be found at https://portal.etsi.org/TB-SiteMap/ESI/Trust-Service-Providers

The Trust Lists of current Trust Service Providers issuing “QCert for ESig” may be found at https://eidas.ec.europa.eu/efda/tl-browser/#/screen/search/type/3?searchCriteria=eyJjb3VudHJpZXMiOlsiQVQiLCJCRSIsIkJHIiwiQ1kiLCJDWiIsIkRFIiwiREsiLCJFRSIsIkVMIiwiRVMiLCJGSSIsIkZSIiwiSFIiLCJIVSIsIklFIiwiSVMiLCJJVCIsIkxJIiwiTFQiLCJMVSIsIkxWIiwiTVQiLCJOTCIsIk5PIiwiUEwiLCJQVCIsIlJPIiwiU0UiLCJTSSIsIlNLIiwiVUsiXSwicVNlcnZpY2VUeXBlcyI6WyJRQ2VydEVTaWciXX0%3D 

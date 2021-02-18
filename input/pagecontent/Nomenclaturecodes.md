11073 20601 uses nomenclature codes to represent an entity that needs to be machine readable such as a type or what the measurement is. Nomenclature codes are 32-bit unsigned integers. The most significant 16 bits give the *partition* and the least significant 16 bits give the *term code*. Partitions group the term codes into sets with a common meaning. For example, in PHD there is a health and fitness partition which groups terms associated with health and fitness, such as term codes for activities like run, bike, swim, altitude gained, distance, etc.

Associated with each 32-bit code is a normative reference identifier. The reference identifier is a 'semi-' human readable string such as MDC_ECG_HEART_RATE which is far easier for the human reader to understand than the associated nomenclature code 147842. However, these reference identifiers are not sent by the PHD as it would occupy too much bandwidth. Since they are not sent in the protocol, this guide does not require the encoder to include them in the FHIR mapping though it is encouraged. A second reason reference identifiers are not required is that is not possible for the encoder to send them if it encounters data from future PHDs using codes it does not know. The new codes can still be mapped to FHIR since they are sent in the protocol, but the reference identifiers require the encoder to have an internal map. Not requiring the reference identifiers allows the encoder to work with these future PHDs. Supporting future compatibility is one of the reasons this guide uses a generic mapping approach.

Units are also encoded using nomenclature codes. In the first version of this implementation guide, these codes were also required to be used in FHIR Quantity data types. However, the HL7 and IHE communities rejected that approach in favor of using UCUM and that approach has been adopted by this guide. To maintain future compatibility, the use of the MDC nomenclature code is only allowed if a UCUM code for the MDC term did not exist, or was not used by PHD standards, at the time the encoder was written.

In FHIR, the 32-bit value of the code is always used. In the PHD to PHG exchange, the 16-bit code is used when the partition can be inferred from the attribute to decrease bandwidth. The encoder must be sure to convert the 16-bit value to the appropriate 32-bit value.

The set of nomenclature codes is extensive, but it is segmented by partitions. At the current time, the codes used in the PHD measurement types and measurement values (when codes) come from the SCADA, INFRA, SITES, PHD_DM, PHD_HF, and PHD_AI partitions. This guide does not restrict the codes to come from only those partitions for future compatibility reasons. New partitions could be added and those codes could be used in future PHD specializations. Since the codes are provided by the PHD, the uploader does not need to maintain a code dictionary unless it wants to include the reference identifier or display text about the code. If this guide were to restrict the allowable codes to a given set of partitions, that restriction would prevent an older implementation from working with future devices when it otherwise could have worked with the device. It is clear, however, that any consumer and interpreter of the uploaded information *would* need to know about the new codes.

More information describing the MDC coding system can be found [here](http://build.fhir.org/mdc.html)

 - [Next: FHIR’s Codeable Concepts](CodeableConcepts.html)
 - [Previous: Mder FLOATs and SFLOATs](MderFLOATsandSFLOATs.html)
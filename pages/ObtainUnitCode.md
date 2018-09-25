---
title: Obtaining the Unit Code
layout: default
active: ObtainingUnitCode
---

Measurements that are quantities (numerics and real-time-sample-arrays) may have units. Though the 11073 20601 specification allows units for enumeration measurements, the use of units for such measurements does not make sense and this profile assumes that enumeration measurements will never have units. In the newer versions of the 20601 specification, units are not allowed in Enumeration objects.

Obtaining the units in most cases is a simple as decoding the Unit-Code attribute. However, the Nu-Observed-Value and Compound-Nu-Observed-Value attributes have their own unit code, and this value overrides the value in the Unit-Code attribute. When these attributes are received applications will need to obtain the unit code from the unit-code subtructure.

11073-20601 unit codes are 11073-10101 MDC values in partition DIM which has a value of 4. The partition value is assumed in the 20601 exchanges and only the term code value of the units is sent. The FHIR encoder will need to create the 32-bit code from the term code and the assumed partition value of 4.
This example shows the mapping of an Android gateway to the Device resource.

<pre>
{
    "resourceType": "Device",
    "id": "ecde3d4e58532d31.000000000000",
    "meta": {
        "profile": [
            "http://hl7.org/fhir/uv/phd/StructureDefinition/PhgDevice"
        ]
    },
    "identifier": [
        {
            "system": "urn:oid:1.2.840.10004.1.1.1.0.0.1.0.0.1.2680",
            "value": "ec-de-3d-4e-58-53-2d-31"
        }
    ],
    "type": {
        "coding": [
            {
                "system": "urn:iso:std:iso:11073:10101",
                "code": "531981"        // This code indicates that it is a Continua gateway
            }
        ],
        "text": "MDC_MOC_VMS_MDS_AHD"
    },
    "version": [
        {
            "type": {
                "coding": [
                    {
                        "system": "urn:iso:std:iso:11073:10101",
                        "code": "532352"
                    }
                ],
                "text": "MDC_REG_CERT_DATA_CONTINUA_VERSION: Continua version"
            },
            "value": "5.0"
        }
    ],
    "property": [
        {
            "type": {
                "coding": [
                    {
                        "system": "urn:iso:std:iso:11073:10101",
                        "code": "68220"
                    }
                ],
                "text": "MDC_TIME_SYNC_PROTOCOL: Time synchronization protocol"
            },
            "valueCode": [
                {
                    "coding": [
                        {
                            "system": "urn:iso:std:iso:11073:10101",
                            "code": "532226"
                        }
                    ],
                    "text": "MDC_TIME_SYNC_NTPV4: "
                }
            ]
        },
        {
            "type": {
                "coding": [
                    {
                        "system": "urn:iso:std:iso:11073:10101",
                        "code": "532353"
                    }
                ],
                "text": "MDC_REG_CERT_DATA_CONTINUA_CERT_DEV_LIST: certified device list as transport-specialization combo"
            },
            "valueCode": [
                {
                    "coding": [
                        {
                            "system": "http://hl7.org/fhir/uv/phd/CodeSystem/ContinuaPHD",
                            "code": "4"
                        }
                    ]
                }
            ]
        },
        {
            "type": {
                "coding": [
                    {
                        "system": "urn:iso:std:iso:11073:10101",
                        "code": "532355"
                    }
                ],
                "text": "MDC_REG_CERT_DATA_CONTINUA_AHD_CERT_LIST: certified Upload classes"
            },
            "valueCode": [
                {
                    "coding": [
                        {
                            "system": "http://hl7.org/fhir/uv/phd/CodeSystem/ContinuaHFS",
                            "code": "0"
                        }
                    ]
                },
                {
                    "coding": [
                        {
                            "system": "http://hl7.org/fhir/uv/phd/CodeSystem/ContinuaHFS",
                            "code": "3"
                        }
                    ]
                },
                {
                    "coding": [
                        {
                            "system": "http://hl7.org/fhir/uv/phd/CodeSystem/ContinuaHFS",
                            "code": "7"
                        }
                    ]
                },
                {
                    "coding": [
                        {
                            "system": "http://hl7.org/fhir/uv/phd/CodeSystem/ContinuaHFS",
                            "code": "2"
                        }
                    ]
                },
                {
                    "coding": [
                        {
                            "system": "http://hl7.org/fhir/uv/phd/CodeSystem/ContinuaHFS",
                            "code": "6"
                        }
                    ]
                }
            ]
        },
        {
            "type": {
                "coding": [
                    {
                        "system": "http://hl7.org/fhir/uv/phd/CodeSystem/ASN1ToHL7",
                        "code": "532354.0"
                    }
                ],
                "text": "regulation-status"
            },
            "valueCode": [
                {
                    "coding": [
                        {
                            "system": "http://terminology.hl7.org/CodeSystem/v2-0136",
                            "code": "Y" // Confusing, correct? A 'Yes' means NOT regulated!
                        }
                    ],
                    "text": "Device is not regulated"
                }
            ]
        }
    ]
}
</pre>
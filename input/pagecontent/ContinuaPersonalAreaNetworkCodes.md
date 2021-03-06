These codes are used to express the Continua Personal Area Network (PHD) interfaces. The codes express both the transport (Bluetooth, USB, etc.) and specialization (Blood pressure, thermometer, glucose, etc.).

<style>table, th, td {
border: 1px solid black;
border-collapse:collapse;
padding: 6px;}</style>

The codes are generated by the following relation:

PHD transport code = transport code X 8192 + (specialization term code - 4096)

The transport code (Tcode) has the following values:

|Transport Code|Transport|
|-
|0|Continua version 1.0|
|1|USB|
|2|Bluetooth HDP|
|3|ZigBee|
|4|Bluetooth Low Energy|
|5|NFC|

The special Tcode of 0 is for Continua version 1.0 when there was no transport component in the reported certified PHD interface codes.

A sample of the most common specialization term codes

|Specialization|MDC term code|Reference Identifier|
|-
|Generic 20601|4169|MDC_DEV_SPEC_PROFILE_GENERIC|
|Pulse Oximeter|4100|MDC_DEV_SPEC_PROFILE_PULS_OXIM|
|Electro cardiograph|4102|MDC_DEV_SPEC_PROFILE_MIN_ECG|
|Blood Pressure Cuff|4103|MDC_DEV_SPEC_PROFILE_BP|
|Thermometer|4104|MDC_DEV_SPEC_PROFILE_TEMP|
|Respiration rate|4109|MDC_DEV_SPEC_PROFILE_RESP_RATE|
|Weight Scale|4111|MDC_DEV_SPEC_PROFILE_SCALE|
|Glucose Monitor|4113|MDC_DEV_SPEC_PROFILE_GLUCOSE|
|Coagulation meter |4114|MDC_DEV_SPEC_PROFILE_COAG|
|Insulin Pump|4115|MDC_DEV_SPEC_PROFILE_INSULIN_PUMP|
|Body Composition Analyizer|4116|MDC_DEV_SPEC_PROFILE_BCA|
|Peak Flow meter|4117|MDC_DEV_SPEC_PROFILE_PEAK_FLOW|
|Sleep Apnea Breathing Equipment|4120| MDC_DEV_SPEC_PROFILE_SABTE|
|Continuous Glucose Monitor|4121|MDC_DEV_SPEC_PROFILE_CGM|
|Cardiovascular Device|4137|MDC_DEV_SPEC_PROFILE_HF_CARDIO|
|Strength Equipment|4138|MDC_DEV_SPEC_PROFILE_HF_STRENGTH|
|Independent Activity/Living Hub|4167|MDC_DEV_SPEC_PROFILE_AI_ACTIVITY_HUB|
|Medication Monitor|4168|MDC_DEV_SPEC_PROFILE_AI_MED_MINDER|
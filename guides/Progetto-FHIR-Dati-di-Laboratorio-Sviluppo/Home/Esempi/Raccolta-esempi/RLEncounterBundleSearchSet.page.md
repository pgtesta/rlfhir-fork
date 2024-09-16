# Esempio con i dati dell'evento clinco 

L'indagine mira a trovare dati di esami effettuati su un paziente durante un certo evento di cura, come un ricovero o una visita. Si cercano dettagli come il codice dell'evento e del paziente, e le date. L'utente sceglie l'evento e filtra gli esami per tipo, data o reparto. 

I parametri da valorizzare per effettuare la ricerca sono:
-	DataFineValidita: data di interesse

| SCOPE |  Esempio con i dati dell'evento clinco|
|---|---|
| VERB | GET |
| BASE | [base_API_Manager]    |
| URL | /Observation?category=laboratory&_include:iterate=Observation:patient&patient.identifier=RSSMRA70A01A399Z&_include=Observation:specimen&_include:iterate=Observation:performer&_include=Observation:encounter  |
|Risposta | {
	"resourceType": "Bundle",
	"id": "esempio-con-encounter",
	"meta": {
		"lastUpdated": "2024-09-10T08:25:11.902+00:00"
	},
	"type": "searchset",
	"total": 2,
	"link": [
		{
			"relation": "self",
			"url": "http://localhost:2777/CDR-FHIR-Endpoint/r4/Observation?_include=Observation%3Aspecimen&_include=Observation%3Aencounter&_include%3Aiterate=Observation%3Apatient&_include%3Aiterate=Observation%3Aperformer&category=laboratory&encounter.date=ge2024-09-05T07%3A30%3A00%2B00%3A00&encounter.date=le2024-09-05T09%3A00%3A00%2B00%3A00&patient.identifier=RSSMRA70A01A399Z"
		}
	],
	"entry": [
		{
			"fullUrl": "http://localhost:2777/CDR-FHIR-Endpoint/r4/Observation/44974389",
			"resource": {
				"resourceType": "Observation",
				"id": "44974389",
				"meta": {
					"versionId": "1",
					"lastUpdated": "2024-09-10T08:09:53.606+00:00",
					"source": "#idMo48jwcs0RrwuD"
				},
				"status": "final",
				"category": [
					{
						"coding": [
							{
								"system": "http://terminology.hl7.org/CodeSystem/observation-category",
								"code": "laboratory",
								"display": "Laboratory"
							}
						]
					}
				],
				"code": {
					"coding": [
						{
							"system": "http://loinc.org",
							"code": "15074-8",
							"display": "Glucose [Moles/volume] in Blood"
						}
					]
				},
				"subject": {
					"reference": "Patient/44974375"
				},
				"encounter": {
					"reference": "Encounter/44974381"
				},
				"effectiveDateTime": "2024-09-05T08:00:00+00:00",
				"performer": [
					{
						"reference": "Practitioner/44974376"
					}
				],
				"valueQuantity": {
					"value": 5.4,
					"unit": "mmol/L",
					"system": "http://unitsofmeasure.org",
					"code": "mmol/L"
				},
				"specimen": {
					"reference": "Specimen/44974384",
					"display": "Blood Specimen"
				}
			},
			"search": {
				"mode": "match"
			}
		},
		{
			"fullUrl": "http://localhost:2777/CDR-FHIR-Endpoint/r4/Observation/44974390",
			"resource": {
				"resourceType": "Observation",
				"id": "44974390",
				"meta": {
					"versionId": "1",
					"lastUpdated": "2024-09-10T08:10:01.337+00:00",
					"source": "#iIbBQqXazKexMSPz"
				},
				"status": "final",
				"category": [
					{
						"coding": [
							{
								"system": "http://terminology.hl7.org/CodeSystem/observation-category",
								"code": "laboratory",
								"display": "Laboratory"
							}
						]
					}
				],
				"code": {
					"coding": [
						{
							"system": "http://loinc.org",
							"code": "718-7",
							"display": "Hemoglobin [Mass/volume] in Blood"
						}
					]
				},
				"subject": {
					"reference": "Patient/44974375"
				},
				"encounter": {
					"reference": "Encounter/44974381"
				},
				"effectiveDateTime": "2024-09-05T08:00:00+00:00",
				"performer": [
					{
						"reference": "Practitioner/44974376"
					}
				],
				"valueQuantity": {
					"value": 13.2,
					"unit": "g/dL",
					"system": "http://unitsofmeasure.org",
					"code": "g/dL"
				},
				"specimen": {
					"reference": "Specimen/44974384",
					"display": "Blood Specimen"
				}
			},
			"search": {
				"mode": "match"
			}
		},
		{
			"fullUrl": "http://localhost:2777/CDR-FHIR-Endpoint/r4/Encounter/44974381",
			"resource": {
				"resourceType": "Encounter",
				"id": "44974381",
				"meta": {
					"versionId": "1",
					"lastUpdated": "2024-09-10T08:05:27.690+00:00",
					"source": "#OWu3W6FKUdoxW3gj"
				},
				"status": "finished",
				"class": {
					"system": "http://terminology.hl7.org/CodeSystem/v3-ActCode",
					"code": "AMB",
					"display": "Ambulatory"
				},
				"subject": {
					"reference": "Patient/44974375"
				},
				"period": {
					"start": "2024-09-05T07:30:00+00:00",
					"end": "2024-09-05T09:00:00+00:00"
				}
			},
			"search": {
				"mode": "include"
			}
		},
		{
			"fullUrl": "http://localhost:2777/CDR-FHIR-Endpoint/r4/Specimen/44974384",
			"resource": {
				"resourceType": "Specimen",
				"id": "44974384",
				"meta": {
					"versionId": "1",
					"lastUpdated": "2024-09-10T08:06:44.973+00:00",
					"source": "#nxb58fdSnJg9gsQw"
				},
				"type": {
					"coding": [
						{
							"system": "http://snomed.info/sct",
							"code": "122555007",
							"display": "Venous blood specimen"
						}
					]
				},
				"subject": {
					"reference": "Patient/44974375"
				},
				"collection": {
					"collectedDateTime": "2023-09-01T07:45:00+00:00"
				},
				"container": [
					{
						"description": "Blood sample for glucose and hemoglobin testing",
						"type": {
							"coding": [
								{
									"system": "http://snomed.info/sct",
									"code": "767390000",
									"display": "Vacutainer tube"
								}
							]
						}
					}
				]
			},
			"search": {
				"mode": "include"
			}
		},
		{
			"fullUrl": "http://localhost:2777/CDR-FHIR-Endpoint/r4/Practitioner/44974376",
			"resource": {
				"resourceType": "Practitioner",
				"id": "44974376",
				"meta": {
					"versionId": "1",
					"lastUpdated": "2024-09-10T08:03:20.825+00:00",
					"source": "#e3TR6j0T8gBTVYVn"
				},
				"identifier": [
					{
						"system": "http://hl7.it/sid/codiceFiscale",
						"value": "BNCGLI80A41D969H"
					}
				],
				"name": [
					{
						"use": "official",
						"family": "Bianchi",
						"given": [
							"Giulia"
						]
					}
				],
				"gender": "female",
				"qualification": [
					{
						"code": {
							"coding": [
								{
									"system": "http://terminology.hl7.org/CodeSystem/v2-0360/2.7",
									"code": "MD",
									"display": "Doctor of Medicine"
								}
							]
						}
					}
				]
			},
			"search": {
				"mode": "include"
			}
		},
		{
			"fullUrl": "http://localhost:2777/CDR-FHIR-Endpoint/r4/Patient/44974375",
			"resource": {
				"resourceType": "Patient",
				"id": "44974375",
				"meta": {
					"versionId": "1",
					"lastUpdated": "2024-09-10T08:02:58.339+00:00",
					"source": "#TuCuIdu3JWOko6HQ"
				},
				"text": {
					"status": "generated",
					"div": "<div xmlns=\"http://www.w3.org/1999/xhtml\"><div class=\"hapiHeaderText\">Mario <b>ROSSI </b></div><table class=\"hapiPropertyTable\"><tbody><tr><td>Identifier</td><td>RSSMRA70A01A399Z</td></tr><tr><td>Date of birth</td><td><span>01 January 1970</span></td></tr></tbody></table></div>"
				},
				"identifier": [
					{
						"system": "http://hl7.it/sid/codiceFiscale",
						"value": "RSSMRA70A01A399Z"
					}
				],
				"name": [
					{
						"use": "official",
						"family": "Rossi",
						"given": [
							"Mario"
						]
					}
				],
				"gender": "male",
				"birthDate": "1970-01-01"
			},
			"search": {
				"mode": "include"
			}
		}
	]
}|

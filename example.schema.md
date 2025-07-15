* fields
	* crop_species
		* type: string
		* description: Crop species (scientific or common name)
		* rdfType: http://aims.fao.org/aos/agrovoc/c_1972
	* crop_yield_kg_per_ha
		* type: number
		* description: Crop yield in kilograms per hectare
		* rdfType: http://aims.fao.org/aos/agrovoc/c_10176
	* planting_date
		* type: date
		* format: yyyy-MM-dd
		* description: Date when the crop was planted
		* rdfType: http://aims.fao.org/aos/agrovoc/c_24065
* primaryKey: crop_species
* missingValues: [""]
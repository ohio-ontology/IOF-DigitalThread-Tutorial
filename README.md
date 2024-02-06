# IOF Digital Thread Tutorial
## How to Download Our Repository
### Downloading a Whole Repository as a ZIP file
1. Go to the main page of the repository by following this link: [IOF-DigitalThread-Tutorial]([(https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial)])
1. Above the list of all files in the repository, locate and select the **<> Code** button. This button allows you to access the repository's code.
![Screenshot 2024-02-05 222956](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/db9c2456-2831-4764-ace2-2663b2efcbde)


1. Then you'll see a dropdown menu. From this menu, choose the option **Download ZIP.** This action will initiate the download of a ZIP file containing our repository's contents.
![Screenshot 2024-02-05 223214](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/f45dbd9e-baa7-483c-adbe-9e8134a044ab)

1. Check your computer's download folder or the location specified in your browser settings to find the downloaded ZIP file. Once you've located it, extract the contents of the ZIP file and save them in a location where you can easily access them in the future.
![Screenshot 2024-02-05 223545](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/d92ee9da-98fd-4f8a-b65a-af7577a6e3b6)

> [!IMPORTANT]
> There are multiple items but make sure you have these three items, as shown in the image below. (folders: examples, ontologies, and a file: iof-digital-thread-tutorial)
> ![Screenshot 2024-02-05 223809](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/a4097274-f461-4558-b6aa-1b9bf4eea5bc)


PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX core: <https://spec.industrialontologies.org/ontology/core/Core/>
PREFIX jeb: <http://simpom.ohio.edu/examples/jet-engine-Base/>
PREFIX jecr: <http://simpom.ohio.edu/examples/jet-engine-cr/>
PREFIX cr: <http://simpom.ohio.edu/ontology/cr/>
SELECT ?engine ?realThrustValue ?designThrustValue ?difference
WHERE { 
# find engine and its thrust 
?engine rdf:type jeb:JetEngine.
 ?spec cr:prescribesProducedEntity ?engine.
?engine core:hasQuality ?thrust.
# find the thrust value 
?thrust core:hasValueExpressionAtAllTimes ?thrustValueExpr.
?thrustValueExpr core:hasSimpleExpressionValue ?realThrustValue.
# find the engine design from associated spec 
?spec cr:prescribesDesignedEntity ?engdesign.
?engdesign core:hasQuality ?thrustdesign.
# find design thrust value 
?thrustdesign core:hasValueExpressionAtAllTimes ?thrustDesignValueExpr.
?thrustDesignValueExpr jeb:hasLowerBoundValue ?designThrustValue.
# compare them 
BIND((?realThrustValue - ?designThrustValue) as ?difference)}

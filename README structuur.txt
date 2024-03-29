README korte uitleg over structuur

Mijn project is opgedeeld in verschillende folders. Dit zijn de stappen die ik
ondernomen heb om dit project uit te voeren.

1. Scraping images
	In deze folder vindt u 2 notebooks.

	Een notebook waarin mijn 2 verschillende pogingen staan om de schilderijen van
	Rembrandt te scrapen (de 2e poging is de poging die dan uiteindelijk de definitieve
	werd).
	Een tweede notebook met daarin de code van de scraping van de schilderijen van
	Vincent Van Gogh.

2. Data exploration & setup
	Hierin vindt u een notebook waarin ik toelicht hoe ik mijn eigen GPU gebruikt heb en
	hoe ik dit opgezet heb. U vindt ook bewijs dat mijn GPU daadwerkelijk ook beschikbaar
	was voor het gebruik van het trainen voor modellen.

	Ook vindt u de data exploration die ik gedaan heb. Data cleanup, een sampling methode
	kiezen en mijn logica erachter, een slideshow van de images in de dataset en ook het 
	opsplitsen van de data in train-, validatie- en testset vindt u in deze notebook.

	De gebruikte functies vindt u in een zelfgeschreven module in de folder "dataset_module".

3. Modellen uit het boek
	In de opgave van de opdracht werd gevraagd om de verschillende modellen uit het boek
	eens toe te passen op de opdracht. 
	Deze code van de verschillende modellen vindt u in de notebook van deze folder.
	De modellen zelf vindt u in de 'models' map in deze folder.

4. Eigen Modellen
	4.1 Eigen Convolutioneel Netwerk
		In deze map vindt u een notebook waarin ik eens mijn eigen convolutionele
		netwerk heb opgesteld voor de classificatie van de schilderijen.
		Ook de getrainde modellen vindt u in deze map.
	
	4.2 CNN met transfer learning
		Hierin vindt u een notebook waarin ik met behulp van transferlearning verschillende
		modellen opstel. Ik maakte gebruik van VGG16 en ResNet.
		Wederom vindt u ook hier de bestanden van de getrainde modellen.

5. Verder experimenteren model

    5.1 Interpretatie gekozen model
        In deze notebook zal ik enkele technieken van hoofdstuk 9 in het boek gebruiken om inzicht te
        verkrijgen naar de werking van mijn gekozen model door middel van plots van de tussentijdse activaties
        van het model. Jammer genoeg ben ik hier niet in geslaagd om dit te doen voor mijn ResNet model,
        dit is wel gelukt voor een CNN die ik zelf heb opgesteld.

    5.2 undersampled strategie

        Hierin vindt u 2 notebooks, namelijk:

            create undersampled dataset.ipynb
                In deze notebook creër ik een dataset met de undersampled strategie die ik dan zal gebruiken om
                mijn gekozen model uit te testen met de undersampled strategie, deze dataset vindt u ook in deze
                folder.
                Hier leg ik ook uit waarom ik besloot om de imbalanced sampling strategie niet uit te proberen.

            uittesten model.ipynb
                In deze notebook test ik dan ook effectief het model uit met een undersampled strategie. Ik doe dit
                zowel zonder als met data augmentation.
                De resultaten van deze modellen vindt u ook deze folder (.keras files).

    5.3 Optimizer & learning rate
        In de notebook die u hier vindt, test ik mijn gekozen model eens uit met de Adam optimizer en verschillende
        learning rates. Hier fine-tune ik mijn model om een zo hoog mogelijke accuracy te bekomen en een zo
        laag mogelijke loss.
        De resultaten van deze modellen vindt u ook deze folder (.keras files).
        Hierin kies ik dan ook mijn finale model.

6. Web App
	In deze folder vindt u de code van mijn webapplicatie die ik gemaakt. Hierop kunt u een
	afbeelding van een schilderij uploaden en mijn model zal dan voorspellen van welke schilder
	dit schilderij geschilderd is.

	U vindt een webApp python file met daarin de Flask code van deze web app.
	Ook een PaintingPredictor python file, die in de webApp file geïmporteerd wordt.
	In deze klasse wordt mijn model ingeladen en is ook verantwoordelijk voor het effectieve
	voorspellen van de images.

Callbacks
    Hierin vindt u de python file waarin ik de callback heb geschreven om de train- en validatie -accuracy & -loss
    in real-time te plotten.

dataset_module
    Dit is een module die ik heb ontwikkeld met daarin de functies die ik gebruik om de dataset te creëren.

datasets
    Deze folder bevat 2 directories, namelijk:

    paintings
        Hierin vindt u de gehele dataset.

    dataset
        Hierin vindt u de dataset opgedeeld in 3 directories -> train, validatie en test.

Documentation
    Hierin vindt u de PDF van het verslag over dit project die ik heb geschreven. Dit verslag dient als ondersteuning
    bij de notebooks in de verschillende stappen.
    Hierin vindt u ook de verschillende versies van de packages die ik gebruikt heb.

used packages.txt
    Dit is een .txt file waarin de gebruikte packages nog eens vermeld staan.











# COVID19_CT_SCAN
In this project, we aim to develop a deep learning model that classifies whether a patient has COVID-19 based on CT scan images of their lungs
* Dans le dossier Data vous trouvez la base de données après transformation (68 images covid19 et 68 autre que covid19) 
* Le code Covid19_CT_SCAN_PreProcessing représente les différentes transformations à partir des CT_SCAN initiaux:
  Détails des transformations de la base de données initiale collecté à partir des services de pneumologies et de radilogie des hopitaux Hédi Chaker et Habib Bourguiba à Sfax:
 - Une moyenne de 512 images CT_SCAN pour chaque patient (136*512 images)
 - Sélection manuelle d'un fenetrage de 260 CT_SCAN pour chaque patient (fenetrage pertinent selon les radiologues)
 - Fusion pour chaque patient des 260 images avec Discrete Wavelet Transform (Réduction de dimension) pour avoir à cette étape : 68 images de patients covid19 et 68 patients malade mais non covid19
 - Transformation des 136 images résultantes en LBP histograms
* Le code Covid19_CNN_best_results représente la modélisation CNN (tensorflow + Keras) ayant donnée les meilleurs résultats avec les images fusionés sans lbp histograms
* Le code Covid19_classification_results représente la modélisation Random Forest, Neural Network, ExtraTree, Gradient Boosting, XGBoost et les meilleurs résultats respectifs (selon la meilleure configuration)

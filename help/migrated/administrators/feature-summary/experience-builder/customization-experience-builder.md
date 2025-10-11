---
title: Personnaliser Experience Builder
jcr-language: en_us
description: Découvrez comment Experience Builder dans Adobe Learning Manager permet une personnalisation approfondie des expériences des élèves.
source-git-commit: a6cd09ba81a41b389ed1ccbea22db6b1966a56e2
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 1%

---


# Personnaliser Experience Builder

## Personnalisation d’un pied de page

Le pied de page s&#39;affiche en bas de l&#39;interface de l&#39;élève et affiche généralement les informations par défaut configurées dans les paramètres de l&#39;administrateur. Les administrateurs peuvent le remplacer par un pied de page personnalisé pour créer une expérience de marque. À l’aide de HTML et CSS, ils peuvent définir la conception, la mise en page et le contenu du pied de page pour répondre aux exigences de l’organisation.

En tant qu’administrateur d’une société de financement, vous pouvez configurer le pied de page à l’aide de l’option personnalisée. Cette option vous permet d’ajouter vos propres HTMLS et feuilles de style CSS, ce qui vous offre une flexibilité totale pour concevoir le pied de page.

Pour personnaliser le pied de page :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]**, puis **[!UICONTROL Général]**.
3. Sélectionnez **[!UICONTROL Modifier]** en regard de l&#39;option **[!UICONTROL Personnalisation du pied de page]**.

   ![](assets/edit-footer.png)
   _Écran Paramètres généraux dans Adobe Learning Manager, affichant les options pour activer la personnalisation du pied de page_

4. Sélectionnez le bouton bascule pour activer la **[!UICONTROL personnalisation du pied de page]**.

   ![](assets/footer-customization-toogle.png)
   _Paramètres de personnalisation du pied de page dans Adobe Learning Manager, affichant le bouton à bascule pour activer le pied de page et les champs personnalisés pour ajouter du HTML ou du code CSS pour le branding personnalisé_

5. Saisissez votre **[!UICONTROL HTML]** et votre **[!UICONTROL CSS]** dans les onglets respectifs.

   ![](assets/type-html-css.png)
   _Écran de personnalisation du pied de page dans Adobe Learning Manager, affichant une section de HTML personnalisée pour ajouter, modifier ou mettre en forme le pied de page de l’interface de l’élève_

6. Sélectionnez **[!UICONTROL Aperçu]** pour afficher le pied de page personnalisé avant de l&#39;enregistrer.

   ![](assets/preview-the-footer.png)
   _Aperçu d’un pied de page personnalisé de l’interface de l’élève dans Adobe Learning Manager, avec des liens catégorisés_

7. Sélectionnez **[!UICONTROL Enregistrer]**.

Le pied de page personnalisé sera affiché à tous les élèves.

## Personnalisation des vignettes de cours

Dans une société financière, les administrateurs peuvent configurer les vignettes de cours pour décider des détails que les élèves voient. Par exemple, ils peuvent afficher la description du cours et le nom de la compétence pour la formation sur la conformité, mais masquer les évaluations ou le nom de l&#39;auteur pour se concentrer sur les exigences obligatoires.

Pour personnaliser les vignettes de cours :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]**, puis **[!UICONTROL Vignette de cours]**.
3. Sélectionnez **[!UICONTROL Modifier]**.

   ![](assets/edit-course-tile.png)
   _Écran des paramètres de mosaïque de cours dans Adobe Learning Manager, affichant l’option Modifier pour personnaliser la mosaïque_

4. Sélectionnez les options ci-dessous pour afficher ou masquer les détails liés aux informations sur le cours :

   a. **[!UICONTROL Format]** : fusionné/individualisé/salle de classe/salle de classe virtuelle : type de l’objet d’apprentissage.
b. **[!UICONTROL Durée]** : durée de l’objet d’apprentissage.
c. **[!UICONTROL Compétence/Produit]** : affichez la compétence ou le produit clé couvert par le cours.
d. **[!UICONTROL Évaluation]** : afficher l’évaluation de l’élève pour le cours.
e. **[!UICONTROL Nom de l&#39;auteur]** : affiche le nom de l&#39;auteur du cours
f. **[!UICONTROL Description (affichée au survol)]** : affichez un court résumé du cours lorsque les élèves survolent la carte.
g. **[!UICONTROL Date de publication/date d’échéance (s’affiche au survol)]** : affichez la date de publication du cours ou la date limite d’achèvement.

5. Sélectionnez les options ci-dessous pour afficher ou masquer les détails liés aux actions de cours :

   a. Bouton **[!UICONTROL Ajouter à la liste d&#39;apprentissage]** : permet aux élèves d&#39;enregistrer le cours dans leur liste d&#39;apprentissage personnelle pour référence ultérieure.
b. **[!UICONTROL Bouton Enregistrer]** : enregistre toutes les modifications apportées aux paramètres ou préférences du cours.
c. Bouton **[!UICONTROL S&#39;inscrire / Continuer]** : permet aux élèves de s&#39;inscrire à un nouveau cours ou de continuer un cours qu&#39;ils ont déjà commencé. Si vous masquez cette option, les actions Ne pas recommander et Télécharger qui s’affichent en regard de cette option seront également supprimées.

   ![](assets/select-details-to-show.png)
   _Écran de configuration de la mosaïque de cours dans Adobe Learning Manager, où les administrateurs sélectionnent les informations et les actions à afficher pour les élèves_

6. Un aperçu de la vignette du cours s’affiche sur le côté droit de l’écran.

   ![](assets/preview-the-course-tile.png)
   _Écran de configuration de la mosaïque de cours dans Adobe Learning Manager, mettant en surbrillance l&#39;aperçu de la mosaïque de cours_

7. Sélectionnez **Enregistrer**.

La vignette de cours personnalisée sera affichée à tous les élèves.

**Avant La Personnalisation**

![](assets/before-customization.png)
_Vignette de cours dans Adobe Learning Manager avant la personnalisation_

**Après la personnalisation**

![](assets/after-customization.png)
_Vignette de cours dans Adobe Learning Manager après la personnalisation_

## Personnalisation à l’aide de JavaScript et CSS

En tant qu&#39;administrateur d&#39;une société financière, vous pouvez personnaliser l&#39;application de l&#39;élève en injectant des feuilles de style CSS et JavaScript correspondant aux exigences de marque et réglementaires de votre entreprise, ce qui vous permet de contrôler entièrement l&#39;apparence, la mise en page et les fonctionnalités interactives de l&#39;application.

Pour personnaliser l’interface de l’élève à l’aide de CSS et JS :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]**, puis **[!UICONTROL Configuration CSS et JS]**.
3. Sélectionnez **[!UICONTROL Modifier]**.
4. Saisissez vos CSS et JS personnalisés dans les onglets respectifs.

   ![](assets/edit-custom-css-js.png)
   Écran de configuration _CSS et JS dans Adobe Learning Manager, où les administrateurs peuvent ajouter des CSS et JS personnalisés_

5. Sélectionnez Enregistrer

La personnalisation sera affichée à tous les élèves.

**Avant la personnalisation**

La conception du menu de la page d’accueil des élèves est basée sur la conception par défaut de Adobe Learning Manager.

![](assets/before-customization.png)
_Page d’accueil de l’élève Adobe Learning Manager avant la personnalisation_

**Après la personnalisation**

Après avoir ajouté les feuilles de style CSS et JS suivantes, le menu de la page d’accueil de l’élève a été mis à jour en fonction de la personnalisation.

Exemple de code CSS :

```
p{
display:block;
}

.withExtraMargin{
margin-right: 100px!important;
}
.alm-footer-extraMargin{
margin-top:0;
}

.alm-layout-almLayoutContainer{
margin: 0;
    margin-bottom: 5rem;
}
#page-756 #category-970151 .alm-category-card-cardLink
{
    height: 400px;

}
#page-756 #category-970151 .alm-category-card-header
{
height: 240px!important;
}
#page-656 .alm-category-card-cardLink{
    height: 380px;
background: white;
}
#page-656 .alm-category-card-header{
height: 200px!important;
}

#page-746 #html-636797 {
    background-color: #f7f9fc;
}

#page-746 .alm-layout-almLayoutContainer{
row-gap:0;
margin-bottom:0;
}

.alm-category-card-cardLink{
transition: border .3s ease;
}
.navText{
       font-size: 16px;
    cursor: pointer;
}
.submenuDownCaret{
display:none;}
.alm-catalog-container-pageContainer{
max-width: 1720px;
    width: 100%;
    padding: 0 40px;
    padding: 0 40px;
}


.pagenavbarcontainer.newNavbarContainer{
width: 1230px;
    margin: 0 auto;
}
div[automationid="learner-menu-inside-header"]{
margin-right:100px!important;
}
#searchScope,.searchSeparator,#searchInDropdown{
display:none!important;
}
#right-navbar{
    margin-right: 0;
}
#companyLogoImg{
cursor:pointer;
max-width:190px;
}
.alm-catalog-container-filtersContainer{
width:340px;
}
.alm-training-card-v2-imageFlipContainer{
border:none;
}
.newSearchBoxContainer{
border-radius: 5px !important;
    border-width: 2px !important;
    border-color: rgb(5, 32, 34) !important;
}
.searchBoxFlex{
width:250px!important;
flex-direction: row-reverse;
    padding-right: 10px;
}
.searchPlaceholderIcon svg{
    height: 16px;
    width: 16px;
}
.searchPlaceholderIcon svg path{
fill: black;
}
#page-656 .alm-layout-almLayoutContainer {
    padding-bottom: 5rem;
margin-bottom:0!important;
}
#page-656 .alm-strip-widget-header-stripHeaderContainer{
display:none;
}
#page-656 .content-wrapper{
padding-bottom:50px;
}
.myspan{
position: absolute;
    bottom: 10px;
    display: block;
    width: 85%;
    margin-left: 20px;
    margin-right: 20px;
    border-top: 1px solid #efefef !important;
    color: #5a697c !important;
    text-align: right;
    padding-top: 5px;
}
.alm-app-wrapperComponent{
padding-bottom:100px;}


@media (max-width: 768px) {
#page-656 .alm-category-widget-cardRow{
   flex-direction: column;
gap: 40px;
 }
#page-656 .alm-category-widget-stripCardContainerRow{
    width: 100%;
    display: flex;
    justify-content: center;
  }
}

@media (max-width: 768px) {
    .container2-right {
        display: none!important;
    }
.container-1 .content-wrapper{
    padding: 0 20px!important;
 }
}
```

Exemple de fichier JS :

```
console.error("Hello Error")

setTimeout(() =>{
// Step 1: Check if #category-284977 is present
const categoryElement = document.querySelector('#category-284977');

if (categoryElement) {
  // Step 2: Find all elements with .alm-category-card-cardLink
  const cardLinks = categoryElement.querySelectorAll('.alm-category-card-cardLink');

  // Step 3: Loop over them and append span with random calculation
  cardLinks.forEach((link, index) => {
    const span = document.createElement('span');



    // Calculate number = (index+1) * 5
    let number = (index + 1) * 5;
if(index === 2){
number = number +2;
}
if(index == 3){
number = number - 7;
}

    span.textContent = `${number} courses`;
    span.classList.add('myspan');
    link.appendChild(span);
  });
}

},2000)
```

![](assets/after-customization-homepage.png)
_Page d’accueil de l’élève Adobe Learning Manager après la personnalisation_

## Personnalisation d’un widget

Les administrateurs peuvent personnaliser les widgets sur les pages personnalisées en appliquant des classes CSS. Par exemple, ils peuvent aligner le texte dans un widget Zone de contenu ou ajuster l’espacement entre les vignettes de cours dans le widget Cours et tracés.

>[!TIP]
>
>Inspect la page de l’élève pour identifier les styles que vous souhaitez modifier. Copiez les classes CSS pertinentes et collez-les dans la page Configuration CSS et JS pour appliquer vos personnalisations.

**Avant la personnalisation**

L’écran suivant affiche la page de formation des ingénieurs commerciaux avant d’ajouter la personnalisation CSS.

![](assets/before-customization-css-js.png)
_Page de l’élève Ingénieur commercial avant la personnalisation_

**Après la personnalisation**

Après avoir ajouté les classes CSS suivantes, la page de l’élève est mise à jour en fonction des styles définis dans ces classes. En fonction de la feuille de style CSS, le texte du widget Zone de contenu a été aligné à gauche et les vignettes de cours sont désormais espacées davantage.

```
.alm-custom-content-box-center {
    align-items: baseline;
    text-align: initial;
}
.alm-training-card-v2-imageContainer {
    border: 14px solid var(--prime-color-white);
    border-radius: -1px;
    height: 106%;
    position: relative;
    transition: all .1s ease-in-out;
}
.alm-course-path-widget-cardRow {
    display: flex;
    gap: 135px;
    margin: 0 0 21px;
    padding: 10px;
}
```

![](assets/after-customization-css-js.png)
_Page de l’élève Ingénieur des ventes après la personnalisation_

### Classes CSS prédéfinies pour les widgets

Vous trouverez ci-dessous quelques classes CSS prédéfinies disponibles pour les widgets.

| Nom du widget | Conteneur CSS |
|---|---|
| Calendrier | alm-calendar-widget-container |
| Catégorie | alm-category-widget-container |
| Cartes de catégorie | alm-category-card-container |
| Conformité | alm-compliance-container |
| Cours et parcours | alm-course-path-widget-container |
| Cartes LO Cours et parcours | alm-training-card-v2-card |
| Zone de contenu | alm-custom-content-box-container |
| Ludification | alm-lead-board-container |
| Apprentissage par les réseaux sociaux | alm-social-learning-container |



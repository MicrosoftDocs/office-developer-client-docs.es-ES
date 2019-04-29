---
title: Variables de plantilla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Las instancias de variables de plantilla (representadas por un elemento templateVariable) especifican los datos de un elemento de fuente de actividad en una plantilla de actividad.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404375"
---
# <a name="template-variables"></a>Variables de plantilla

Las instancias de variables de plantilla (representadas por un elemento **templateVariable** ) especifican los datos de un elemento de fuente de actividad en una plantilla de actividad. 
  
Para obtener un ejemplo de XML de fuente de actividades, consulte ejemplo de XML de la [fuente de actividades](activity-feed-xml-example.md).

En la siguiente tabla se muestran los tipos de variables de plantilla admitidas, cada una de ellas representada por el valor de enumeración XML correspondiente.
  
|**Tipo de variable de plantilla**|**Descripción**|
|:-----|:-----|
|**entityVariable** <br/> |Una persona, un grupo o un elemento.  <br/> |
|**linkVariable** <br/> |Un vínculo.  <br/> |
|**listVariable** <br/> |Un grupo de objetos.  <br/> |
|**pictureVariable** <br/> |Imagen.  <br/> |
|**publisherVariable** <br/> |El publicador del elemento fuente de actividades.  <br/> |
|**textVariable** <br/> |Un bloque de texto.  <br/> |
   
Cada tipo de variable de plantilla tiene elementos necesarios para especificar los datos de esa variable. Las variables de plantilla se especifican de la siguiente manera:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Variable de plantilla de lista

Puede especificar variables de plantilla que están contenidas en una lista (delimitadas por los elementos **listVariable** y **ListItems** ) de la siguiente manera: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Una variable de plantilla del tipo **listVariable** es un contenedor de objetos. Puede contener elementos delimitados por comas (del tipo **linkVariable** o **textVariable** ) o imágenes (del tipo **pictureVariable** ). Las listas pueden contener hasta cinco elementos de vínculo, cinco elementos de texto o cinco imágenes. 
  
Outlook Social Connector (OSC) localiza el vínculo o los elementos de lista de texto de acuerdo con la configuración regional del sistema de Windows.
  
Para analizar y mostrar correctamente imágenes en un elemento de fuente de actividad, debe incluir imágenes en una lista. Todas las imágenes tienen un tamaño de 52 píxeles de alto. No se cambia el ancho de la imagen.
  
## <a name="template-variable-elements"></a>Elementos de variable de plantilla

En esta sección se describen los elementos obligatorios y opcionales admitidos para cada tipo de variable de plantilla.
  
### <a name="entityvariable"></a>entityVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**id** <br/> |IDENTIFICADOR único del usuario. Necesario.  <br/> |
|**nameHint** <br/> |Nombre que se va a mostrar en el elemento de la fuente. Opcional.  <br/> |
|**profileUrl** <br/> |La dirección URL del perfil de la persona que se usará como hipervínculo para el nombre de la persona en el elemento de la fuente, si el nombre de la persona está presente. Opcional.  <br/> |
|**emailAddress** <br/> |La dirección de correo electrónico que se usa para actualizar la información de contacto de esta persona en Outlook. Opcional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**value** <br/> |La dirección URL de este vínculo. Necesario.  <br/> |
|**text** <br/> |El texto del vínculo que se va a mostrar en lugar de la propia dirección URL. Opcional.  <br/> |
   
### <a name="listvariable"></a>listVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**listItems** <br/> |Un contenedor para los elementos de la lista. Necesario.  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**value** <br/> |Dirección URL de la imagen. Necesario.  <br/> |
|**altText** <br/> |Texto alternativo que se va a mostrar para la accesibilidad y cuando el usuario mueve el puntero del mouse sobre la imagen. Opcional.  <br/> |
|**href** <br/> |Hipervínculo que se va a usar cuando el usuario haga clic en la imagen, si el destino deseado no es la dirección URL de la imagen especificada por el elemento **Value** . Opcional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**id** <br/> |IDENTIFICADOR único del usuario. Necesario.  <br/> |
|**nameHint** <br/> |Nombre que se va a mostrar en el elemento de la fuente. Opcional.  <br/> |
|**profileUrl** <br/> |La dirección URL del perfil de la persona que se usará como hipervínculo para el nombre de la persona en el elemento de la fuente, si el nombre de la persona está presente. Opcional.  <br/> |
|**emailAddress** <br/> |La dirección de correo electrónico que se usa para actualizar la información de contacto de esta persona en Outlook. Opcional.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**value** <br/> |Texto que se va a mostrar. Opcional.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Información general sobre XML para un elemento de fuente de actividades](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityDetails](activitydetails-element.md)  
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Directrices para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)  
- [XML para actividades](xml-for-activities.md)  
- [Esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)


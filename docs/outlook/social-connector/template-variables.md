---
title: Variables de plantilla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Las instancias de variables de plantilla (representadas por un elemento templateVariable) especifican los datos de un elemento de fuente de actividades en una plantilla de actividad.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404375"
---
# <a name="template-variables"></a>Variables de plantilla

Las instancias de variables de plantilla (representadas por un **elemento templateVariable)** especifican los datos de un elemento de fuente de actividades en una plantilla de actividad. 
  
Para obtener un ejemplo de XML de fuente de actividades, vea [el ejemplo XML de fuente de actividades](activity-feed-xml-example.md).

En la tabla siguiente se muestran los tipos de variables de plantilla admitidas, cada una representada por el valor de enumeración XML correspondiente.
  
|**Tipo de variable de plantilla**|**Descripción**|
|:-----|:-----|
|**entityVariable** <br/> |Una persona, grupo o cosa.  <br/> |
|**linkVariable** <br/> |Un vínculo.  <br/> |
|**listVariable** <br/> |Un grupo de objetos.  <br/> |
|**pictureVariable** <br/> |Imagen.  <br/> |
|**publisherVariable** <br/> |El publicador del elemento de fuente de actividades.  <br/> |
|**textVariable** <br/> |Bloque de texto.  <br/> |
   
Cada tipo de variable de plantilla tiene elementos necesarios para especificar los datos sobre esa variable. Las variables de plantilla se especifican de la siguiente manera:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Variable de plantilla de lista

Puede especificar variables de plantilla contenidas en una lista (delimitadas por los elementos **listVariable** y **listItems)** de la siguiente manera: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Una variable de plantilla del tipo **listVariable** es un contenedor para objetos. Puede contener elementos delimitados por comas (del tipo **linkVariable** o **textVariable)** o imágenes (del tipo **pictureVariable).** Las listas pueden contener hasta cinco elementos de vínculo, cinco elementos de texto o cinco imágenes. 
  
Outlook Social Connector (OSC) localiza los elementos de lista de vínculos o texto de acuerdo con la configuración regional del sistema de Windows.
  
Para analizar y mostrar imágenes correctamente en un elemento de fuente de actividades, debe incluir imágenes en una lista. Se cambia el tamaño de todas las imágenes a 52 píxeles de alto. No se cambia el tamaño del ancho de la imagen.
  
## <a name="template-variable-elements"></a>Elementos de variable de plantilla

En esta sección se tratan los elementos obligatorios y opcionales admitidos para cada tipo de variable de plantilla.
  
### <a name="entityvariable"></a>entityVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**id** <br/> |Identificador único del usuario. Necesario.  <br/> |
|**nameHint** <br/> |Nombre que se mostrará en el elemento de fuente. Opcional.  <br/> |
|**profileUrl** <br/> |Dirección URL del perfil de la persona que se usará como hipervínculo para el nombre de la persona en el elemento de fuente, si el nombre de la persona está presente. Opcional.  <br/> |
|**emailAddress** <br/> |La dirección de correo electrónico que se usa para actualizar la información de contacto de esta persona en Outlook. Opcional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**value** <br/> |Dirección URL de este vínculo. Necesario.  <br/> |
|**text** <br/> |Texto del vínculo que se mostrará en lugar de la dirección URL en sí. Opcional.  <br/> |
   
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
|**altText** <br/> |Texto alternativo que se va a mostrar para accesibilidad y cuando el usuario mueve el puntero del mouse sobre la imagen. Opcional.  <br/> |
|**href** <br/> |El hipervínculo que se usará cuando el usuario haga clic en la imagen, si el destino deseado no es la dirección URL de imagen especificada por el **elemento de** valor. Opcional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**id** <br/> |Identificador único del usuario. Necesario.  <br/> |
|**nameHint** <br/> |Nombre que se mostrará en el elemento de fuente. Opcional.  <br/> |
|**profileUrl** <br/> |Dirección URL del perfil de la persona que se usará como hipervínculo para el nombre de la persona en el elemento de fuente, si el nombre de la persona está presente. Opcional.  <br/> |
|**emailAddress** <br/> |La dirección de correo electrónico que se usa para actualizar la información de contacto de esta persona en Outlook. Opcional.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Elemento**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Necesario.  <br/> |
|**value** <br/> |Texto que se mostrará. Opcional.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Información general sobre XML para un elemento de fuente de actividades](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityDetails](activitydetails-element.md)  
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Directrices para mostrar actividades correctamente](guidelines-for-properly-displaying-activities.md)  
- [XML para actividades](xml-for-activities.md)  
- [Esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)


---
title: Variables de plantilla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instancias de variables de plantilla (representadas por un elemento templateVariable) especifican los datos de una fuente de elemento en una plantilla de actividad de actividades.
ms.openlocfilehash: 99f4c2de586447fb0361e528bcd33d62b79e0fb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821237"
---
# <a name="template-variables"></a>Variables de plantilla

Instancias de variables de plantilla (representadas por un elemento **templateVariable** ) especifican los datos de una fuente de elemento en una plantilla de actividad de actividades. 
  
Para obtener un ejemplo de la actividad de fuente XML, vea [Ejemplo de XML de fuente de actividad](activity-feed-xml-example.md).

En la siguiente tabla muestra a los tipos de variables de plantilla admitidos, que cada uno de ellos representado por el valor de enumeración de XML correspondiente.
  
|**Tipo de variable de plantilla**|**Descripción**|
|:-----|:-----|
|**entityVariable** <br/> |Una persona, un grupo o una cosa.  <br/> |
|**linkVariable** <br/> |Un vínculo.  <br/> |
|**listVariable** <br/> |Un grupo de objetos.  <br/> |
|**pictureVariable** <br/> |Imagen.  <br/> |
|**publisherVariable** <br/> |El publicador de la actividad de fuente de elemento.  <br/> |
|**textVariable** <br/> |Un bloque de texto.  <br/> |
   
Cada tipo de variable de plantilla necesario elementos para especificar los datos sobre esa variable. Variables de plantilla se especifican de la siguiente manera:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Variable de plantilla de lista

Puede especificar variables de plantilla que están dentro de una lista (delimitada por los elementos **listVariable** y **listItems** ) como se indica a continuación: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Una variable de la plantilla del tipo de **listVariable** es un contenedor de objetos. Puede contener elementos delimitado por comas (del tipo **linkVariable** o **textVariable** ) o imágenes (del tipo **pictureVariable** ). Listas pueden contener hasta cinco vincular elementos, cinco elementos de texto o imágenes de cinco. 
  
Outlook Social Connector (OSC) localiza elementos de lista de vínculo o texto según la configuración regional del sistema de Windows.
  
Para analizar y mostrar las imágenes en un elemento de fuente de actividades correctamente, debe incluir las imágenes en una lista. Se cambia el tamaño de todas las imágenes para ser 52 píxeles de alto. El ancho de la imagen no se cambia el tamaño.
  
## <a name="template-variable-elements"></a>Elementos de variables de plantilla

En esta sección se describe los elementos requeridos y opcionales admitidos para cada tipo de variable de plantilla.
  
### <a name="entityvariable"></a>entityVariable

|**Element**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Obligatorio.  <br/> |
|**id** <br/> |Identificador único del usuario. Obligatorio.  <br/> |
|**nameHint** <br/> |El nombre que se mostrará en el elemento de la fuente. Opcional.  <br/> |
|**profileUrl** <br/> |La dirección URL del perfil de la persona que se usará como el hipervínculo para el nombre de la persona en el elemento de la fuente, si está presente el nombre de persona. Opcional.  <br/> |
|**emailAddress** <br/> |La dirección de correo electrónico que se usa para actualizar la información de contacto de esta persona en Outlook. Opcional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Element**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Obligatorio.  <br/> |
|**value** <br/> |La dirección URL para este vínculo. Obligatorio.  <br/> |
|**text** <br/> |El texto del vínculo para mostrar en lugar de la propia dirección URL. Opcional.  <br/> |
   
### <a name="listvariable"></a>listVariable

|**Element**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Obligatorio.  <br/> |
|**listItems** <br/> |Un contenedor para los elementos de la lista. Obligatorio.  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**Element**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Obligatorio.  <br/> |
|**value** <br/> |La dirección URL de la imagen. Obligatorio.  <br/> |
|**altText** <br/> |El texto alternativo para mostrar para la accesibilidad y cuando el usuario mueve el puntero del mouse sobre la imagen. Opcional.  <br/> |
|**href** <br/> |El hipervínculo que se utilizará cuando el usuario hace clic en la imagen, si el destino deseado no es la dirección URL de imagen especificada por el elemento de **valor** . Opcional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Element**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Obligatorio.  <br/> |
|**id** <br/> |Identificador único del usuario. Obligatorio.  <br/> |
|**nameHint** <br/> |El nombre que se mostrará en el elemento de la fuente. Opcional.  <br/> |
|**profileUrl** <br/> |La dirección URL del perfil de la persona que se usará como el hipervínculo para el nombre de la persona en el elemento de la fuente, si está presente el nombre de persona. Opcional.  <br/> |
|**emailAddress** <br/> |La dirección de correo electrónico que se usa para actualizar la información de contacto de esta persona en Outlook. Opcional.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Element**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre de la variable. Obligatorio.  <br/> |
|**value** <br/> |El texto para mostrar. Opcional.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elemento de la fuente de información general de XML de una actividad](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityDetails](activitydetails-element.md)  
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Instrucciones para mostrar correctamente las actividades](guidelines-for-properly-displaying-activities.md)  
- [XML de actividades](xml-for-activities.md)  
- [Esquema XML de proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)


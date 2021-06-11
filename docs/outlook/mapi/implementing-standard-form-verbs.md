---
title: Implementación de verbos de formulario estándar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426124"
---
# <a name="implementing-standard-form-verbs"></a>Implementación de verbos de formulario estándar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define un conjunto de verbos estándar, o acciones realizadas cuando un usuario realiza una selección de menú o hace clic en un botón, que todos los visores de formularios deben admitir. Cada verbo tiene una constante asociada para su identificación, definida en EXCHFORM. Archivo de encabezado H. En la tabla siguiente se enumeran los verbos de formulario estándar y sus constantes asociadas:
  
|**Verb**|**Valor**|
|:-----|:-----|
|Abrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Responder  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Responder a todos  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Reenviar  <br/> |EXCHIVERB_FORWARD  <br/> |
|Imprimir  <br/> |EXCHIVERB_PRINT  <br/> |
|Guardar como  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Responder en carpeta  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Cuando un usuario elija un verbo, pase su constante en una llamada al método [IMAPIForm::D oVerb](imapiform-doverb.md) del formulario para realizar su acción correspondiente. 
  
Además de tener acceso a verbos a través del visor de formularios, los usuarios a veces pueden tener acceso a verbos directamente desde el formulario. Por ejemplo, algunos objetos de formulario permiten al usuario invocar el verbo **Imprimir** haciendo clic con el botón secundario en el formulario y eligiendo **Imprimir** en un menú contextual. 
  


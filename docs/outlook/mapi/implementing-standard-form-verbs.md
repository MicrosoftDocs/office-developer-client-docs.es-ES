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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317447"
---
# <a name="implementing-standard-form-verbs"></a>Implementación de verbos de formulario estándar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define un conjunto de verbos estándar o acciones realizadas cuando un usuario hace una selección de menú o hace clic en un botón, que deben admitir todas las vistas de formulario. Cada verbo tiene una constante asociada para la identificación, definida en el EXCHFORM. H archivo de encabezado. En la siguiente tabla se enumeran los verbos de formulario estándar y sus constantes asociadas:
  
|**Verb**|**Value**|
|:-----|:-----|
|Abrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Respuesta  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Responder a todos  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Forward  <br/> |EXCHIVERB_FORWARD  <br/> |
|Print  <br/> |EXCHIVERB_PRINT  <br/> |
|Guardar como  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Responder en carpeta  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Cuando un usuario elige un verbo, pasa su constante en una llamada al método [IMAPIForm::D overb](imapiform-doverb.md) del formulario para realizar su acción correspondiente. 
  
Además de tener acceso a los verbos a través del visor de formularios, los usuarios pueden tener acceso a verbos directamente desde el formulario. Por ejemplo, algunos objetos Form permiten al usuario invocar el verbo **Imprimir** haciendo clic con el botón secundario en el formulario y eligiendo **Imprimir** desde un menú contextual. 
  


---
title: Implementación de una tabla de One-Off contenedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417423"
---
# <a name="implementing-a-container-one-off-table"></a>Implementación de una tabla de One-Off contenedor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para obtener acceso a la tabla de uso único que pertenece a uno de los contenedores, MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con la interfaz **IMAPITable.** Se pide al contenedor que devuelva su tabla de uso único cuando una aplicación cliente intenta agregar un destinatario al contenedor. Si el contenedor permite a algún destinatario, el proveedor puede devolver su propia implementación de tabla o llamar a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) para devolver la implementación MAPI. 
  
El conjunto de plantillas de la tabla de uso único del contenedor debe reflejar el tipo de destinatarios que puede contener el contenedor en particular. Normalmente, esto incluye una o dos plantillas, plantillas para crear un usuario de mensajería individual o una lista de distribución. Los identificadores de entrada de estas plantillas se mantienen en las propiedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) y **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Sin embargo, los contenedores no están limitados a estos tipos de entradas. Pueden contener otros tipos de destinatarios o entradas que no son destinatarios, como directorios. 
  


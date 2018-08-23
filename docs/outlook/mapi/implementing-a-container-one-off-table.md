---
title: Implementar una tabla puntual de contenedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d468943f84f1d23f1b4b84881e69cee0041a5bae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576599"
---
# <a name="implementing-a-container-one-off-table"></a>Implementar una tabla puntual de contenedor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para obtener acceso a la tabla de uso único que pertenecen a uno de los contenedores, MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con el **IMAPITable** interfaz. El contenedor se le pide que devuelva su tabla de uso único cuando una aplicación cliente intenta agregar a un destinatario al contenedor. Si el contenedor permite a los destinatarios, su proveedor puede devolver su propia implementación de la tabla o llamar a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) para devolver la implementación de MAPI. 
  
El conjunto de plantillas en la tabla de uso único de contenedor debe reflejar el tipo de destinatarios que puede contener el contenedor determinado. Normalmente, esto incluye uno o dos plantillas, plantillas para la creación de un usuario de mensajería individual o una lista de distribución. Los identificadores de entrada para estas plantillas se conservan en las propiedades de **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) y **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)). Sin embargo, los contenedores de ninguna manera se limitan a estos tipos de entradas. Pueden contener otros tipos de destinatarios o de las entradas de destinatario que no sean tales como los directorios. 
  


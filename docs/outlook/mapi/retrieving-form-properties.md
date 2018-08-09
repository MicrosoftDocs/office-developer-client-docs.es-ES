---
title: Recuperar propiedades de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820532"
---
# <a name="retrieving-form-properties"></a>Recuperar propiedades de formulario

  
  
**Hace referencia a**: Outlook 
  
Para ejecutar una consulta que sea significativa para un tipo de mensaje personalizado, una aplicación necesita conocer las propiedades que se esperan en ese mensaje. Para obtener una lista de propiedades que usa una clase de mensaje personalizada, una aplicación cliente consulta el Administrador de formularios de MAPI. El Administrador de formulario obtiene esta información desde el archivo de configuración de forma adecuada para que las aplicaciones cliente pueden usar esta información sin la sobrecarga de activar el formulario del propio servidor. Para ello, la aplicación cliente llama al método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) de la siguiente manera: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Tenga en cuenta que el tercer argumento para **ResolveMessageClass** es la carpeta que contiene la tabla de contenido asociada que la consulta buscará los servidores del formulario. NULL indica que el Administrador de formulario debe buscar en todos los contenedores de formulario disponibles. Si la consulta es ejecutar en una carpeta determinada, es mejor incluir el puntero [IMAPIFolder](imapifolderimapicontainer.md) apropiado en su lugar. 
  
## <a name="see-also"></a>Vea también



[Interacciones del servidor de formulario](form-server-interactions.md)


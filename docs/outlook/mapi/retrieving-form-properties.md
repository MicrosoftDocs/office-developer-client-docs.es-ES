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
ms.openlocfilehash: a6636b6298fcf565a297ed5df8a885c43c279c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583851"
---
# <a name="retrieving-form-properties"></a>Recuperar propiedades de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para ejecutar una consulta que sea significativa para un tipo de mensaje personalizado, una aplicación necesita conocer las propiedades que se esperan en ese mensaje. Para obtener una lista de propiedades que usa una clase de mensaje personalizada, una aplicación cliente consulta el Administrador de formularios de MAPI. El Administrador de formulario obtiene esta información desde el archivo de configuración de forma adecuada para que las aplicaciones cliente pueden usar esta información sin la sobrecarga de activar el formulario del propio servidor. Para ello, la aplicación cliente llama al método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) de la siguiente manera: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Tenga en cuenta que el tercer argumento para **ResolveMessageClass** es la carpeta que contiene la tabla de contenido asociada que la consulta buscará los servidores del formulario. NULL indica que el Administrador de formulario debe buscar en todos los contenedores de formulario disponibles. Si la consulta es ejecutar en una carpeta determinada, es mejor incluir el puntero [IMAPIFolder](imapifolderimapicontainer.md) apropiado en su lugar. 
  
## <a name="see-also"></a>Recursos adicionales



[Interacciones del servidor de formulario](form-server-interactions.md)


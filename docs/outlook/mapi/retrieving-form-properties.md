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
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328654"
---
# <a name="retrieving-form-properties"></a>Recuperar propiedades de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para emitir una consulta que sea significativa para un tipo de mensaje personalizado, una aplicación debe conocer las propiedades que se esperan en el mensaje. Para obtener una lista de las propiedades que usa una clase de mensaje personalizada, una aplicación cliente consulta el administrador de formularios MAPI. El administrador de formularios obtiene esta información del archivo de configuración de formulario apropiado para que las aplicaciones cliente puedan usar esta información sin la sobrecarga de activar el servidor de formularios en sí. Para ello, la aplicación cliente llama al método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) de la siguiente manera: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Tenga en cuenta que el tercer argumento de **ResolveMessageClass** es la carpeta que contiene la tabla de contenido asociada en la que la consulta buscará los servidores de formularios. NULL indica que el administrador de formularios debe buscar en todos los contenedores de formularios disponibles. Si la consulta se va a ejecutar en una carpeta determinada, es mejor incluir el puntero [IMAPIFolder](imapifolderimapicontainer.md) apropiado en su lugar. 
  
## <a name="see-also"></a>Vea también



[InterAcciones del servidor de formularios](form-server-interactions.md)

